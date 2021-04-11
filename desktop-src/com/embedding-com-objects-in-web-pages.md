---
title: Inserindo objetos COM em páginas da Web
description: Você pode usar objetos COM em páginas da Web. Para fazer isso, primeiro crie uma instância do objeto COM. Depois que uma instância de objeto é criada, você pode usá-la em scripts subsequentes nessa página da Web.
ms.assetid: 7e2c9da7-aeae-4206-8be9-1303240b2b1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4762dd01d4bc07aab5c0b146c56cdb1aec3cb28f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292033"
---
# <a name="embedding-com-objects-in-web-pages"></a>Inserindo objetos COM em páginas da Web

Você pode usar objetos COM em páginas da Web. Para fazer isso, primeiro crie uma instância do objeto COM. Depois que uma instância de objeto é criada, você pode usá-la em scripts subsequentes nessa página da Web.

Para criar uma instância de objeto COM em uma página da Web, você pode usar uma marca de objeto. Como alternativa, se a linguagem de script fornecer uma maneira nativa de criar objetos COM, você poderá criar uma instância de objeto usando script.

Observe que a inserção de objetos COM em páginas da Web só funciona com navegadores que dão suporte a ActiveX e COM, por exemplo, o Internet Explorer.

O exemplo a seguir ilustra o uso da marca OBJECT para inserir um objeto COM em uma página da Web:

``` syntax
<OBJECT 
  ID = vid 
  CLASSID = "clsid:31263EC0-2957-11CF-A1E5-00AA9EC79700" 
  BORDER = 0 
  VSPACE = 0 
  HSPACE = 0 
  ALIGN = TOP 
  HEIGHT = 100% 
  WIDTH = 100%
>
</OBJECT>
 
```

Você também pode criar uma instância de objeto COM no script, se a linguagem de script fornecer uma maneira de criar objetos COM. Por exemplo, o VBScript fornece o método CreateObject e o JScript fornece o objeto ActiveXobject. A criação de objetos no script é ilustrada nos exemplos a seguir.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Dim objXL
  Set objXL = CreateObject("Excel.Application")
</SCRIPT>
 
<SCRIPT LANGUAGE = "JScript">
  var objXL = new ActiveXObject("Excel.Application");
</SCRIPT>
 
```

Além do método CreateObject e do objeto ActiveXobject, o VBScript e o JScript fornecem o método GetObject, que retorna uma instância de objeto.

Depois que um objeto COM tiver sido criado, você poderá referenciá-lo em scripts subsequentes usando o identificador especificado no atributo ID da marca do objeto. No exemplo anterior, esse identificador foi especificado como "vid". Observe que o script que usa o objeto COM deve aparecer após a marca de objeto ou o script que cria a instância do objeto; caso contrário, o identificador de objeto será indefinido. O script a seguir usa o objeto objXL para exibir as informações de versão do Microsoft Excel.

``` syntax
<SCRIPT LANGUAGE = "VBScript">
  Msgbox objXL.Version
</SCRIPT>
 
```

Se você estiver escrevendo scripts inseridos em uma página da Web, o navegador também expõe um modelo de objeto que seus scripts podem acessar. O modelo usado pelo Internet Explorer está em conformidade com o Modelo de Objeto do Documento (DOM) proposto pelo World Wide Web Consortium (W3C).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando scripts com objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




