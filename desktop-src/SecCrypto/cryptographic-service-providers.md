---
description: Importante essa API é preterida.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Provedores de serviço de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370645"
---
# <a name="cryptographic-service-providers"></a>Provedores de serviço de criptografia

> [!IMPORTANT]
> Essa API está preterida. O software novo e o existente devem começar a usar [APIs de próxima geração de criptografia.](/windows/desktop/SecCNG/cng-portal) A Microsoft poderá remover essa API em versões futuras.

 

Um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) contém implementações de algoritmos e padrões de criptografia. No mínimo, um CSP consiste em uma dll ( [*biblioteca de vínculo dinâmico*](../secgloss/d-gly.md) ) que implementa as funções no [*CryptoSPI*](../secgloss/c-gly.md) (uma interface de [*programa do sistema*](../secgloss/s-gly.md)). A maioria dos CSPs contém a implementação de todas as suas próprias funções. Alguns CSPs, no entanto, implementam suas funções principalmente em um programa de serviço baseado no Windows gerenciado pelo Gerenciador de controle de serviços do Windows. Outras implementam funções em hardware, como um [*cartão inteligente*](../secgloss/s-gly.md) ou um co-processador seguro. Se um CSP não implementar suas próprias funções, a DLL atuará como uma camada de passagem, facilitando a comunicação entre o sistema operacional e a implementação do CSP real.

Esta seção inclui os seguintes tópicos.



| Tópico                                                                                      | Sumário                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipos de provedor criptográfico](cryptographic-provider-types.md)                           | Os tipos de provedor criptográfico são famílias de provedores de serviços de criptografia que compartilham formatos de dados e protocolos criptográficos. Os formatos de dados incluem esquemas de [*preenchimento*](../secgloss/p-gly.md) de algoritmos, [*comprimentos de chave*](../secgloss/k-gly.md)e modos padrão. |
| [Provedores de serviços de criptografia da Microsoft](microsoft-cryptographic-service-providers.md) | Informações detalhadas sobre os CSPs disponíveis atualmente na Microsoft.                                                                                                                                                                                                                                                                                       |



 

 

 
