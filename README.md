# Estudos_Asp.Net

# .Net Framework VS .Net Core - Qual é a diferença ?

- ASP.NET Web Application (.NET Framework) 
  - cria o dotnet Framework na ultima versao. 
    - FullFreamWock e a juntar todas as versao do asp.net.

-  A view dos dois nao muda e igual para as duas versao 
-  O controler muda so o return
  
    ```aspnet 
    
    // .Net Framework e um action result que chama uma view 
    
    public ActionResult Index()
    {
       return view();
    }
    ```
    
     
    ```aspnet 
    
    // .Net Core tem o retorno chamada a view porem tem um retorno diferente 
    
    public IActionResult Index()
    {
       return view();
    }
    ```
     
- .Net core e mais rapido do que o asp.net Framework
- O core e closs plataforma.
- pode trabalha com docker.

* Considere usar o .NET Framework levando em conta os seguintes fatores:
- Você não vai necessitar de um suporte multiplataforma para sua aplicação;

- Você precisa de um ambiente estável;

- Você precisa realizar atualizações frequentes;

- Você já esta trabalhando em um aplicativo que a .NET Framework e vai estender suas funcionalidades;

- Você já possui  um equipe com experiência na .NET Framework;

- Você precisa do suporte ao Visual Basic

- Você vai criar aplicações desktop Windows Forms ou WPF

- Você vai desenvolver aplicações ASP .NET Web Forms

- Você precisa usar os recursos do WCF , WF e Worflow Services

- Você tem receio de novidades;


* Considere usar o .NET Core se:

- Você deseja segmentar suas aplicações nos sistemas operacionais Windows, Linux e Mac;

- Você esta disposto a realizar ajustes e atualizações visto que o .NET Core ainda não é maduro;

- Você esta disposto a aprender coisas novas e quer estar na vanguarda;


#  Tipos de Variáveis  e Conversões 
o c# tem o tipo de variáveis forte
- mais Utilizado
  - string: e um conjunto de char 2 bits para cada letra
  - int: 4 byte e tipo para inteiros
  - float: 4 byte e para pontos flutuantes menor uso moedas
  - double: 8 byte e para pontos flutuantes maior
  - boolean (verdadeiro ou falso) 0 e 1
  - decimal 16 byte e para pontos flutuantes grande
  - char 2 byte
  - long 8 byte 
  - byte 1 byte

## Conversões 
-  Convert.toString()
-  toInt()
-  toFloat()
 
 * tipo de conversões 
 - um class stact
 - cast (var variavl = (int) '1')
 
 # Operadores logicos e Condicionais
 
 * Condicionais
  - if 
  - switch
* tipos Condicionais
  - Commun (if/else)
  - Case(switch)
  - Ternario (1 == 1 ? true ? false)
 
 * Operadores
  - == Igual
  - ! Not
  - != Diferente 
  - && E
  - || ou
  - < maior  
  - > menor
  - +
  - -
  - *
  - /

# ActionResults               
  ## Type                     Helper Method
  - viewResult                View()
  - PartialViweResult         PartialView()
  - ContentResult             Content()  
  - RedirectResult            Redirect()
  - RedirectToRouteResult     RedirectToAction()
  - JsonResult                Json()
  - FileResult                File()
  - HttpNotFoundResult        HttpNotFound()
  - EmpptyResult  
 
# Criando Rotas 

```
// no controler acima do metodo
   [Route("caminho/{id}/{nome}")]
 
 ou
 
 //Route Config
 routes.MapRoute("minhaPrimeiraRotar",
 "editarPlanos/{planoid}/{nome}",
 new { controller = "Plano", action = "Edit" });
```
