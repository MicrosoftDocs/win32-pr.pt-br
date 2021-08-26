---
description: Importante Esta API foi preterida.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Provedores de serviços criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7ef58122e47594b195700241b936b8985cd88137c52841976495b195d7e4c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876186"
---
# <a name="cryptographic-service-providers"></a>Provedores de serviços criptográficos

> [!IMPORTANT]
> Essa API está preterida. Os softwares novos e existentes devem começar [a usar Cryptography Next Generation APIs.](/windows/desktop/SecCNG/cng-portal) A Microsoft pode remover essa API em versões futuras.

 

Um [*CSP (provedor de serviços*](../secgloss/c-gly.md) criptográficos) contém implementações de padrões criptográficos e algoritmos. No mínimo, um CSP consiste em uma DLL (biblioteca de [*vínculo*](../secgloss/d-gly.md) dinâmico) que implementa as funções no [*CryptoSPI*](../secgloss/c-gly.md) (uma interface de programa [*do sistema).*](../secgloss/s-gly.md) A maioria dos CSPs contém a implementação de todas as suas próprias funções. Alguns CSPs, no entanto, implementam suas funções principalmente em um programa de serviço baseado em Windows gerenciado pelo Windows de controle de serviço. Outros implementam funções em hardware, como um [*cartão inteligente*](../secgloss/s-gly.md) ou coprocessador seguro. Se um CSP não implementar suas próprias funções, a DLL atuará como uma camada de passagem, facilitando a comunicação entre o sistema operacional e a implementação real do CSP.

Esta seção inclui os seguintes tópicos.



| Tópico                                                                                      | Sumário                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipos de provedor criptográfico](cryptographic-provider-types.md)                           | Os tipos de provedor criptográfico são famílias de provedores de serviços criptográficos que compartilham formatos de dados e protocolos criptográficos. Os formatos de dados incluem esquemas [*de preenchimento de*](../secgloss/p-gly.md) algoritmos, [*comprimentos de chave*](../secgloss/k-gly.md)e modos padrão. |
| [Provedores de Serviços Criptográficos da Microsoft](microsoft-cryptographic-service-providers.md) | Informações detalhadas sobre CSPs atualmente disponíveis na Microsoft.                                                                                                                                                                                                                                                                                       |



 

 

 
