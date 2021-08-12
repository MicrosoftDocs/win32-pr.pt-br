---
description: Quando um objeto é ativado em um determinado contexto, chamadas subsequentes para ou dele, dentro do contexto, são tratadas de maneira diferente das chamadas no limite de contexto.
ms.assetid: 9e234b41-f269-4674-adc4-12018277a14b
title: Interceptação de chamadas entre contextos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3a969479419b75313f8b439f3cf9ffc7b94946e9007752ccc4e99a54cd6ad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547833"
---
# <a name="interception-of-cross-context-calls"></a>Interceptação de chamadas entre contextos

Quando um objeto é ativado em um determinado contexto, chamadas subsequentes para ou dele, dentro do contexto, são tratadas de maneira diferente das chamadas no limite de contexto. As chamadas no limite de contexto são tratadas com proxies leves. Esses proxies lidam com qualquer mediação necessária para ajustar o ambiente de tempo de run-time de um que acomoda o chamador para um que acomoda o chamador. Esse processo é conhecido como *interceptação*.

A interceptação de chamada entre contextos é necessária porque os objetos em contextos diferentes têm requisitos de tempo de executar diferentes – esse é precisamente o motivo dos contextos. O COM+ intercepta todas as referências de objeto que você passa como parâmetros de método e as converte automaticamente em proxies para que elas sejam usáveis no novo contexto.

Se você compartilhar referências de objeto entre limites de contexto por outros meios, por exemplo, em variáveis globais, sempre deverá usar [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). Essas funções podem converter uma referência de objeto em um proxy que pode ser usado em um contexto diferente. Nunca compartilhe uma referência de objeto bruto entre limites de contexto.

O comportamento de chamadas em todo o contexto pode ter consequências indesejadas no caso de objetos expondo interfaces que não podem ser empacotadas. Nessa circunstância, é provável que você queira dizer que o objeto que não pode ser marshalado seja ativado somente no contexto de seu chamador e nunca em seu próprio contexto. Você pode fazer isso selecionando a opção **Deve ser** ativada  no contexto do chamador na guia Ativação da página **Propriedades do** componente. (Consulte [Impor a ativação no contexto do chamador](enforcing-activation-in-the-caller-s-context.md) para obter instruções passo a passo.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ativação de contexto](context-activation.md)
</dt> </dl>

 

 
