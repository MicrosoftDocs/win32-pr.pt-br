---
description: Um provedor não é necessário para dar suporte a operações de instância parcial. No entanto, um provedor deve dar suporte a toda a semântica de uma operação de instância parcial, processar uma instância completa ou retornar \_ um \_ parâmetro WBEM E sem suporte \_ .
ms.assetid: bc498655-ad6d-44f5-912d-9b7ee95825ec
ms.tgt_platform: multiple
title: Suporte a operações de Partial-Instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2043c09ca129acab6976cabda2b854be464d26036cb5b9df1bc5b82989ccc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922846"
---
# <a name="supporting-partial-instance-operations"></a>Suporte a operações de Partial-Instance

Um provedor não é necessário para dar suporte a operações de instância parcial. No entanto, um provedor deve dar suporte a toda a semântica de uma operação de instância parcial, processar uma instância completa ou retornar um **\_ \_ \_ parâmetro WBEM E sem suporte**.

Ao criar um provedor que dá suporte a operações de instância parcial, você deve observar as seguintes regras:

-   Reutilize o mesmo objeto de contexto que o WMI envia para o provedor. O WMI usa o \_ \_ \_ \_ valor nomeado "obter \_ solicitação de cliente ext" para evitar deadlocks e remove esse cliente antes de encaminhar o objeto de contexto para um provedor.
-   Para chamadas reentrantes no WMI que não exigem uma operação de instância parcial, certifique-se de repassar o mesmo objeto de contexto sem modificações. O WMI recebe o objeto de contexto sem o \_ \_ \_ valor nomeado "Get ext \_ cliente \_ Request" definido e exclui todos os valores nomeados associados a operações de instância parcial do objeto de contexto antes de passá-lo para outros provedores. Não alterar o objeto de contexto impede que outros provedores recebam operações de recuperação de instância parcial destinadas a um objeto diferente e não relacionado.
-   Para executar uma operação reentrante na instância parcial ao realizar uma solicitação, defina o \_ \_ \_ \_ valor nomeado e a propriedade "obter solicitação de cliente ext \_ " ausente. Opcionalmente, você pode modificar as propriedades no \_ \_ \_ valor nomeado "obter \_ Propriedades ext" antes de enviar o objeto de contexto de volta ao WMI com a chamada reentrante.
-   Não acesse o objeto de contexto depois de devolvê-lo ao WMI durante uma chamada reentrante. outros provedores podem modificar as listas de propriedades ou outros valores durante a reentrância. Você pode examinar ou modificar o objeto de contexto somente pela duração da chamada de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) implementada.

 

 



