---
title: Navegando para outras lojas online
description: Navegando para outras lojas online
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player online, navegando
- lojas online, navegando
- tipo 2 lojas online, navegando
- navegando em lojas online do tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1b2cb120ac161fd92bf8d35826b9dc096c95c37d916f19eb2aeb7362aabe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574429"
---
# <a name="navigating-to-other-online-stores"></a>Navegando para outras lojas online

Você pode criar links para outras lojas online que você possui ou vincular entre lojas online fornecidas por outras pessoas. Para fazer isso, você precisa saber o nome da chave da loja online para a qual você deseja navegar.

O código de exemplo a seguir mostra o HTML que cria um link para alternar do proseware online store para o recurso "ServiceTask2" da loja online southhere Video:


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



Quando o usuário clica no link, Windows Media Player solicita ao usuário para alternar para o armazenamento de Vídeos south ltd. Se o usuário permitir, o Player alterna armazenará e navegará até o painel de tarefas especificado, ao mesmo tempo que os parâmetros da cadeia de caracteres de consulta. Os parâmetros de cadeia de caracteres de consulta mostrados no exemplo anterior são parâmetros personalizados. Isso significa que a loja online para a que você alterna deve esperar esses valores e lidar com eles. Sua loja online (e qualquer loja para a qual você alternar) pode usar parâmetros de cadeia de caracteres de consulta da maneira que você escolher.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Navegando entre painéis de tarefa de serviço**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navegação para lojas online do tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




