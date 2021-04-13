---
title: Usando objetos COM em páginas Active Server
description: Você pode criar scripts de objetos COM em aplicativos de Active Server Pages (ASP).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5d73244ce5bd6c56deeda9bf4e3e4986b3d4039
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291848"
---
# <a name="using-com-objects-in-active-server-pages"></a>Usando objetos COM em páginas Active Server

Você pode criar scripts de objetos COM em aplicativos de Active Server Pages (ASP). Para fazer isso, você deve primeiro criar uma instância do objeto usando a marca OBJECT ou chamando o método CreateObject do objeto do servidor ASP. Depois que um objeto COM tiver sido criado, você poderá usá-lo em scripts subsequentes na página ASP.

Usando o ASP, você pode trabalhar com muitos tipos diferentes de mecanismos de script, cada um com suporte para uma linguagem de script diferente. O ASP vem com os mecanismos de script VBScript e JScript. Você também pode conectar mecanismos de script desenvolvidos por outras empresas para dar suporte a idiomas como PerlScript, PScript, Python e outros.

Se você não definir a linguagem de script para uma página ASP, o VBScript será o padrão. Para especificar uma linguagem de script diferente do VBScript, inclua uma linha como a seguinte na parte superior de cada página ASP:

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Para usar um objeto COM em uma página ASP, você deve primeiro criar uma instância desse objeto. Você faz isso usando a marca OBJECT e especificando o valor "SERVER" para o atributo RUNAT, conforme mostrado no exemplo a seguir. Por padrão, a marca OBJECT cria uma instância do objeto no cliente. Definir o atributo RUNAT como servidor faz com que o objeto seja criado no servidor. O objeto deve ser executado no servidor para ser usado pelo ASP.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

Você também pode criar uma instância de um objeto COM em uma página ASP chamando o método CreateObject do objeto do servidor ASP. O uso de Server. CreateObject é mais lento do que criar o objeto usando uma marca de objeto, mas é um pouco mais legível porque especifica o identificador programático em vez do identificador de classe do objeto COM. O objeto Server é exposto pelo ASP e não precisa ser criado. Como chamar Server. CreateObject é ilustrado nos exemplos a seguir. O primeiro exemplo é o VBScript:

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

O exemplo a seguir é JScript:

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

Chamar CreateObject é mais lento do que usar a marca OBJECT para criar um objeto COM. Em aplicativos em que o desempenho é crítico, você deve usar a marca OBJECT.

Depois de criar uma instância do objeto COM, você pode usá-la em scripts. Fazer isso é ilustrado no exemplo de VBScript a seguir, que define o valor da propriedade border do objeto COM.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando scripts com objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




