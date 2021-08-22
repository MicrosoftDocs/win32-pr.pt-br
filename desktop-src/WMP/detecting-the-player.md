---
title: Detectando o Player
description: Detectando o Player
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player lojas online, detectando jogadores
- lojas online, detectando jogadores
- Digite 1 lojas online, detectando jogadores
- Digite 2 lojas online, detectando jogadores
- Windows Media Player lojas online, detecção de Player
- lojas online, detecção de Player
- tipos 1 lojas online, detecção de Player
- tipo 2 lojas online, detecção de Player
- detecção de Player
- detectando jogadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d511fc8c14a901c6823715293c5eb621b45762cd5e9fae78d8c4df503a03bf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863506"
---
# <a name="detecting-the-player"></a>Detectando o Player

Ao criar uma página da Web para sua loja online, você pode decidir que deseja que os usuários consigam exibir a página em um navegador ou em Windows Media Player. Você pode usar um script ASP para determinar se sua página da Web está hospedada no Player.

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



Observe que o código anterior pressupõe que o parâmetro de versão existe na cadeia de caracteres de consulta quando hospedado em Windows Media Player. Isso é verdadeiro para páginas abertas pelo usuário, mas podem não ser verdadeiras para páginas abertas usando **external. NavigateTaskPaneURL**. Para que a cadeia de consulta de versão exista durante a navegação programaticamente, você deve adicionar o parâmetro version à chamada de método ou acrescentar dinamicamente a versão à URL base do elemento **Navigate** do seu documento serviceInfo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o documento do serviceInfo dinamicamente**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




