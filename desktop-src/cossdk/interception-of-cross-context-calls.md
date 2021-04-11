---
description: Quando um objeto é ativado em um determinado contexto, as chamadas subsequentes para ou dele, dentro do contexto, são manipuladas de forma diferente do que as chamadas no limite de contexto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Interceptação de chamadas de contexto cruzado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d70bc8bff83d02b13656f9854f0e6d16cd4e173
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296101"
---
# <a name="interception-of-cross-context-calls"></a>Interceptação de chamadas de contexto cruzado

Quando um objeto é ativado em um determinado contexto, as chamadas subsequentes para ou dele, dentro do contexto, são manipuladas de forma diferente do que as chamadas no limite de contexto. Chamadas entre o limite de contexto são manipuladas com proxies leves. Esses proxies tratam de qualquer mediação necessária para ajustar o ambiente de tempo de execução de um que acomoda o chamador para um que acomode o receptor. Esse processo é conhecido como *interceptação*.

A interceptação de chamada entre contexto é necessária porque os objetos em contextos diferentes têm requisitos de tempo de execução diferentes — isso é precisamente o motivo para contextos. O COM+ intercepta todas as referências de objeto que você passa como parâmetros de método e as converte automaticamente em proxies para que elas sejam utilizáveis no novo contexto.

Se você compartilhar referências de objeto entre limites de contexto por outros meios — por exemplo, em variáveis globais — você deve sempre usar [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). Essas funções podem converter uma referência de objeto em um proxy utilizável em um contexto diferente. Nunca compartilhe uma referência de objeto bruto entre limites de contexto.

O comportamento de chamadas entre o contexto pode ter consequências indesejadas no caso de objetos expondo interfaces que não podem ser empacotadas. Nessa circunstância, é provável que você queira insistir que o objeto que não pode ser empacotado seja ativado somente no contexto de seu chamador e nunca em seu próprio contexto. Você pode fazer isso selecionando a opção **deve ser ativada no contexto do chamador** na guia **ativação** da página **Propriedades** do componente. (Consulte [impondo a ativação no contexto do chamador](enforcing-activation-in-the-caller-s-context.md) para obter instruções passo a passo.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ativação de contexto](context-activation.md)
</dt> </dl>

 

 
