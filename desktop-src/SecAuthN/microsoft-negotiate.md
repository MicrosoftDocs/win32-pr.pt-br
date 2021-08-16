---
description: O Microsoft Negotiate é um provedor de suporte de segurança que atua como uma camada de aplicativo entre a Interface do Provedor de Suporte de Segurança e os outros SSPs.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Negociação da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd223267a2e7d0e4dc23ae356a6fa2e6224c742c491e428369f15fb6d46ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786948"
---
# <a name="microsoft-negotiate"></a>Negociação da Microsoft

O Microsoft Negotiate é [*um*](../secgloss/s-gly.md) SSP (provedor de suporte de segurança) que atua como uma camada de aplicativo entre o [SSPI](sspi.md) [*(Security Support Provider Interface)*](../secgloss/s-gly.md) e os outros SSPs. Quando um aplicativo chama o SSPI para fazer logoff em uma rede, ele pode especificar um SSP para processar a solicitação. Se o aplicativo especificar Negotiate, Negotiate analisará a solicitação e escolherá o melhor SSP para lidar com a solicitação com base na política de segurança configurada pelo cliente.

Atualmente, o pacote de segurança Negotiate seleciona entre [Kerberos](microsoft-kerberos.md) e [NTLM.](microsoft-ntlm.md) Negotiate seleciona Kerberos, a menos que ele não possa ser usado por um dos sistemas envolvidos na autenticação ou o aplicativo de chamada não forneceu informações suficientes para usar o Kerberos.

Para permitir que Negotiate selecione o provedor de segurança [Kerberos,](microsoft-kerberos.md) o aplicativo cliente deve fornecer um SPN [*(nome*](../secgloss/s-gly.md) da entidade de serviço), um NOME UPN ou um nome de conta NetBIOS como o nome de destino. Caso contrário, Negotiate sempre selecionará o [provedor de segurança NTLM.](microsoft-ntlm.md)

Um servidor que usa o pacote Negotiate é capaz de responder a aplicativos cliente que selecionam especificamente o provedor de segurança [Kerberos](microsoft-kerberos.md) ou [NTLM.](microsoft-ntlm.md) No entanto, um aplicativo cliente deve saber que um servidor dá suporte ao pacote Negotiate para solicitar autenticação usando Negotiate. Um servidor que não dá suporte a Negotiate nem sempre pode responder a solicitações de clientes que especificam Negociar como o SSP.

## <a name="reasons-to-use-the-negotiate-package"></a>Motivos para usar o pacote Negotiate

-   Permite que o sistema use o protocolo mais forte (mais seguro) disponível.
-   Garante a compatibilidade de encaminhamento para seu aplicativo.
-   Garante que seu aplicativo exibe o comportamento que está de acordo com a política de segurança definida pelo cliente.

 

 
