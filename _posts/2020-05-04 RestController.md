RestController
---

controller와 RestController 차이


**Controller  - Url 요청에 따라 View랑 Mapping 처리함**
최상위 클래스 위에 @RequestMapping("/")로 한번에 공통 매핑위치 처리
@Autowired Service를 통해 service의 method를 이용
적절한 ResponseEntity(DTO)를 body에 담아 Client에 반환

@Controller
API와 view를 동시에 사용하는 경우에 사용
대신 API 서비스로 사용하는 경우는 @ResponseBody를 사용하여 객체를 반환한다.
view(화면) return이 주목적



**RestController - API 처리위주 서비스에서 사용 View 는 X VERSION 4부터)**


@Controller

@RequestMapping("/user")

public class UserController {

	

	@RequestMapping( value="/json/{id}", method = RequestMethod.GET)

	@ResponseBody

	public UserModel getByIdInJSON( @PathVariable String id){
@RequestMapping -> @ResponseBody
data(json, xml 등) return이 주목적: return ResponseEntity
@RestController = @Controller + @ResponseBody



