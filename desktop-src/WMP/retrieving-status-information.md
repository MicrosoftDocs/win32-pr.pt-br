---
title: Recuperando informações de status
description: Recuperando informações de status
ms.assetid: 61561520-705a-4d06-a72c-c1cc6315f54e
keywords:
- Lojas online do Windows Media Player, Gerenciador de download
- lojas online, Gerenciador de download
- tipo 2 lojas online, Gerenciador de download
- Armazenamentos online do Windows Media Player, recuperando status
- lojas online, recuperando status
- tipo 2 lojas online, recuperando status
- Windows Media Player, Gerenciador de download
- Gerenciador de download do Windows Media Player
- Gerenciador de download
- Recuperando status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 155d1c9d949306ae5cda3ffff6a7a55fd3bae23c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636642"
---
# <a name="retrieving-status-information"></a>Recuperando informações de status

As informações de status são atualizadas usando o temporizador criado na função **init** . Todo o status é atualizado usando o mesmo temporizador. O nome da função para o evento de timer é **OnTimer**.

**OnTimer** determina as informações a serem exibidas com base na seleção de usuário, que é armazenada na variável global chamada g \_ oCurrentDLItem. A função primeiro testa se os valores de tamanho ou de progresso são válidos e cria uma cadeia de caracteres para cada caso.


```C++
var Size = g_oCurrentDLItem.size <=0 ? "Waiting..." : g_oCurrentDLItem.size + " bytes";
var Progress = g_oCurrentDLItem.progress <=0 ? "Waiting..." : g_oCurrentDLItem.progress + " bytes";

```



Se um valor for válido, a cadeia de caracteres representará a contagem de bytes. Se o valor não for válido, como-1, a cadeia de caracteres fornecerá uma mensagem para informar ao usuário que as informações ainda não estão disponíveis.

Em seguida, um bloco de **opção** determina se o download do item selecionado foi concluído ou cancelado. Se qualquer um dos casos for verdadeiro, o valor do tamanho ou do progresso das variáveis será atualizado de acordo.


```C++
switch(g_oCurrentDLItem.downloadState)
{
    case 3:            
        Size = "Completed";
        Progress = "Completed";
        break;
        
    case 4:
        Size = "Canceled";
        Progress = "Canceled";
        break;
        
    default:
        break;                
}

```



Por fim, as informações de status são exibidas no elemento DIV chamado dlstate.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o Gerenciador de download**](using-the-download-manager.md)
</dt> </dl>

 

 




