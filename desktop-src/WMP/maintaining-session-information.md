---
title: Mantendo informações da sessão
description: Mantendo informações da sessão
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Armazenamentos online do Windows Media Player, mantendo informações de sessão
- lojas online, mantendo informações de sessão
- Digite 2 lojas online, mantendo as informações da sessão
- Armazenamentos online do Windows Media Player, informações da sessão
- lojas online, informações da sessão
- Digite 2 lojas online, informações da sessão
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- mantendo informações da sessão
- informações da sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292859"
---
# <a name="maintaining-session-information"></a>Mantendo informações da sessão

## <a name="how-the-sample-stores-information"></a>Como o exemplo armazena informações

A página da Web de exemplo mantém dados usando cookies. Os cookies são simplesmente pares de nome/valor persistentes que o navegador da Web pode armazenar para você.

Quando a página da Web é fechada, a função de **desligamento** é executada. **Shutdown** chama a função **SetPendingCookies**. Essa função faz um loop pela lista de coleta de download, armazenada na caixa de listagem suspensa chamada selDLC. Se uma coleção de download contiver itens incompletos, a função chamará o método **SetCookie**, passando um nome e um valor. A cadeia de caracteres de nome é determinada acrescentando um valor inteiro a um valor constante, **WMPDLC**, que é armazenado na variável chamada g \_ sPreCookie. Por exemplo, para a terceira coleção de download pendente, o nome do cookie seria "WMPDLC2", porque o mecanismo de contagem é baseado em zero. À medida que cada cookie é criado, a função incrementa a variável global g \_ pendente para manter uma contagem de downloads pendentes. O código é reproduzido aqui para sua conveniência:


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



**IsDLCComplete** é uma função auxiliar que simplesmente executa loops em cada item de download da coleção de download para determinar se algum item está pendente. Se houver um item pendente, a função retornará false.

**SetCookie** é a função que cria o cookie.

Quando **SetPendingCookies** retorna, o **desligamento** cria o cookie de contagem, que armazena o valor da variável g \_ pendente. Esse valor é importante porque a página da Web precisa de uma maneira de determinar quantos cookies serão recuperados quando recarregados. O nome do cookie de contagem é armazenado na variável chamada g \_ sCountCookie.

## <a name="how-the-sample-retrieves-information"></a>Como o exemplo recupera informações

Quando a página da Web é carregada, a função **init** é executada. Primeiro, a função chama **GetPendingDlCount** para recuperar o cookie de contagem. Em seguida, ele armazena esse valor na variável chamada g \_ pendente. Em seguida, ele chama a função **PopulateDLList** para recuperar cada cookie de sessão de download e adiciona seu identificador à caixa de listagem suspensa. Este é o código para essa função:


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



A função **clearlist** remove todos os itens da caixa de listagem.

Em seguida, a função entra em um loop. Cada nome de cookie é criado como uma cadeia de caracteres e, em seguida, o cookie é recuperado chamando a função auxiliar **GetCookie**. Depois de recuperados, o cookie é excluído chamando **DelCookie**. Se o cookie tiver um valor, o valor será adicionado à caixa de listagem. Essa ação inicia o evento **onChange** para a lista selDLC, que, por sua vez, chama a função de manipulador denominada **OnSelectDLC**. Essa é a mesma função que é executada quando o usuário seleciona uma coleção de download; é o código que preenche a caixa de listagem baixar item.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Gerenciador de download**](using-the-download-manager.md)
</dt> </dl>

 

 




