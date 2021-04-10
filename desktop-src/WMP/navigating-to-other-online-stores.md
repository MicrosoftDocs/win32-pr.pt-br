---
title: Navegando para outras lojas online
description: Navegando para outras lojas online
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Lojas online do Windows Media Player, navegando
- lojas online, navegando
- Digite 2 lojas online, navegando
- navegando no tipo 2 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291762"
---
# <a name="navigating-to-other-online-stores"></a>Navegando para outras lojas online

Você pode criar links para outras lojas online que você possui ou entre links para lojas online fornecidas por outras pessoas. Para fazer isso, você precisa saber o nome da chave para a loja online na qual deseja navegar.

O código de exemplo a seguir mostra o HTML que cria um link para alternar da loja online da Proseware para o recurso "ServiceTask2" da loja online de vídeo Southridge:


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



Quando o usuário clica no link, o Windows Media Player solicita que o usuário alterne para o armazenamento de vídeo Southridge. Se o usuário permitir, o Player alternará os armazenamentos e navegará até o painel de tarefas especificado, acrescentando os parâmetros da cadeia de caracteres de consulta. Os parâmetros de cadeia de caracteres de consulta mostrados no exemplo anterior são parâmetros personalizados. Isso significa que a loja online que você alterna para deve esperar esses valores e tratá-los. Sua loja online (e qualquer loja que você alternar para) pode usar parâmetros de cadeia de caracteres de consulta da maneira que você escolher.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Navegando entre os painéis de tarefas de serviço**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navegação para lojas online do tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




