---
title: Usando objetos COM em Active Server páginas
description: Você pode fazer script de objetos COM Active Server aplicativos ASP (páginas de script).
ms.assetid: 3a074360-8b6c-4cb6-813b-73863fe11c46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8ba1bbdd0729a8893b1c28d1a2347fc5ddea04c8d0de4e1ea413e765ab8df4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896195"
---
# <a name="using-com-objects-in-active-server-pages"></a>Usando objetos COM em Active Server páginas

Você pode fazer script de objetos COM Active Server aplicativos ASP (páginas de script). Para fazer isso, primeiro você deve criar uma instância do objeto usando a marca OBJECT ou chamando o método CreateObject do objeto ASP Server. Depois que um objeto COM tiver sido criado, você poderá usá-lo em scripts subsequentes na página ASP.

Usando o ASP, você pode trabalhar com muitos tipos diferentes de mecanismos de script, cada um dos quais dá suporte a uma linguagem de script diferente. O ASP vem com OVBScript e JScript de script. Você também pode conectar mecanismos de script desenvolvidos por outras empresas para dar suporte a linguagens como PerlScript, PScript, Python e outras.

Se você não definir a linguagem de script para uma página ASP, o VBScript será o padrão. Para especificar uma linguagem de script diferente do VBScript, inclua uma linha como a seguinte na parte superior de cada página do ASP:

``` syntax
<%@ LANGUAGE=JScript %>
 
```

Para usar um objeto COM em uma página ASP, primeiro você deve criar uma instância desse objeto. Faça isso usando a marca OBJECT e especificando o valor "SERVER" para o atributo RUNAT, conforme mostrado no exemplo a seguir. Por padrão, a marca OBJECT cria uma instância do objeto no cliente. Definir o atributo RUNAT como SERVER faz com que o objeto seja criado no servidor. O objeto deve ser executado no servidor para ser usado pelo ASP.

``` syntax
<OBJECT 
RUNAT=SERVER 
ID=MyAds 
CLASSID="Clsid:1621F7C0-60AC-11CF-9427-444553540000">
</OBJECT> 
 
```

Você também pode criar uma instância de um objeto COM em uma página ASP chamando o método CreateObject do objeto servidor ASP. Usar Server.CreateObject é mais lento do que criar o objeto usando uma marca OBJECT, mas é um pouco mais acessível porque especifica o identificador programático em vez do identificador de classe do objeto COM. O objeto Server é exposto pelo ASP e não precisa ser criado. Como chamar Server.CreateObject é ilustrado nos exemplos a seguir. O primeiro exemplo é VBScript:

``` syntax
<% 
  Set MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

O próximo exemplo é JScript:

``` syntax
<% 
  var MyAds = Server.CreateObject("MSWC.AdRotator") 
%>
 
```

Chamar CreateObject é mais lento do que usar a marca OBJECT para criar um objeto COM. Em aplicativos em que o desempenho é crítico, você deve usar a marca OBJECT.

Depois de criar uma instância do objeto COM, você pode usá-la em scripts. Isso é ilustrado no exemplo de VBScript a seguir, que define o valor da propriedade Border do objeto COM.

``` syntax
<% MyAds.Border = 0 %>
 
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Scripts com objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




