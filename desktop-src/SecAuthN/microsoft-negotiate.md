---
description: O Microsoft Negotiate é um provedor de suporte de segurança que atua como uma camada de aplicativo entre a interface do provedor de suporte de segurança e os outros SSPs.
ms.assetid: 3aa7e979-8b55-416d-bed1-28296055d38e
title: Microsoft Negotiate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ce57a8f8924120dcce51e50e05de90fd6774b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920854"
---
# <a name="microsoft-negotiate"></a>Microsoft Negotiate

O Microsoft Negotiate é um SSP ( [*provedor de suporte de segurança*](../secgloss/s-gly.md) ) que atua como uma camada de aplicativo entre o [SSPI](sspi.md)( [*Security Support Provider interface*](../secgloss/s-gly.md) ) e outros SSPs. Quando um aplicativo chama o SSPI para fazer logon em uma rede, ele pode especificar um SSP para processar a solicitação. Se o aplicativo especificar Negotiate, Negotiate analisará a solicitação e escolherá o melhor SSP para lidar com a solicitação com base na política de segurança configurada pelo cliente.

Atualmente, o pacote de segurança Negotiate seleciona entre [Kerberos](microsoft-kerberos.md) e [NTLM](microsoft-ntlm.md). Negociar seleciona Kerberos, a menos que não possa ser usado por um dos sistemas envolvidos na autenticação ou o aplicativo de chamada não forneceu informações suficientes para usar o Kerberos.

Para permitir que o Negotiate selecione o provedor de segurança [Kerberos](microsoft-kerberos.md) , o aplicativo cliente deve fornecer um [*nome da entidade de serviço*](../secgloss/s-gly.md) (SPN), um nome UPN ou um nome de conta NetBIOS como o nome de destino. Caso contrário, Negotiate sempre seleciona o provedor de segurança [NTLM](microsoft-ntlm.md) .

Um servidor que usa o pacote Negotiate é capaz de responder a aplicativos cliente que selecionam especificamente o provedor de segurança [Kerberos](microsoft-kerberos.md) ou [NTLM](microsoft-ntlm.md) . No entanto, um aplicativo cliente deve saber que um servidor dá suporte ao pacote Negotiate para solicitar autenticação usando Negotiate. Um servidor que não dá suporte a Negotiate nem sempre responde a solicitações de clientes que especificam Negotiate como o SSP.

## <a name="reasons-to-use-the-negotiate-package"></a>Motivos para usar o pacote Negotiate

-   Permite que o sistema use o protocolo mais forte (mais seguro) disponível.
-   Garante a compatibilidade de encaminhamento para seu aplicativo.
-   Garante que seu aplicativo exiba o comportamento que está de acordo com a política de segurança definida pelo cliente.

 

 
