---
title: Detectando o Player
description: Detectando o Player
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Lojas online do Windows Media Player, detectando jogadores
- lojas online, detectando jogadores
- Digite 1 lojas online, detectando jogadores
- Digite 2 lojas online, detectando jogadores
- Repositórios online do Windows Media Player, detecção de Player
- lojas online, detecção de Player
- tipos 1 lojas online, detecção de Player
- tipo 2 lojas online, detecção de Player
- detecção de Player
- detectando jogadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916349"
---
# <a name="detecting-the-player"></a>Detectando o Player

Ao criar uma página da Web para sua loja online, você pode decidir que deseja que os usuários consigam exibir a página em um navegador ou no Windows Media Player. Você pode usar um script ASP para determinar se sua página da Web está hospedada no Player.

O código de exemplo a seguir recupera o parâmetro de versão da cadeia de caracteres de consulta de URL para determinar se a página está hospedada no Windows Media Player:


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



Observe que o código anterior pressupõe que o parâmetro de versão existe na cadeia de caracteres de consulta quando hospedado no Windows Media Player. Isso é verdadeiro para páginas abertas pelo usuário, mas podem não ser verdadeiras para páginas abertas usando **external. NavigateTaskPaneURL**. Para que a cadeia de consulta de versão exista durante a navegação programaticamente, você deve adicionar o parâmetro version à chamada de método ou acrescentar dinamicamente a versão à URL base do elemento **Navigate** do seu documento serviceInfo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o documento do serviceInfo dinamicamente**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




