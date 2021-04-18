---
description: O sistema operacional Windows dá suporte à autenticação usando pacotes de segurança que funcionam como ambos os provedores de suporte de segurança e como pacotes de autenticação.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Provedor de suporte de segurança/pacotes de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749891"
---
# <a name="security-support-providerauthentication-packages"></a>Provedor de suporte de segurança/pacotes de autenticação

O sistema operacional Windows dá suporte à autenticação usando [*pacotes de segurança*](../secgloss/s-gly.md) que funcionam como ambos os provedores de [*suporte de segurança*](../secgloss/s-gly.md) e como pacotes de [*autenticação*](../secgloss/a-gly.md). Os pacotes de segurança fornecem os serviços de suporte do processo de logon de um pacote de autenticação do Windows e também fornecem serviços de autenticação para aplicativos implementando um conjunto de funções que são mapeadas para a SSPI ( [interface do provedor de suporte de segurança](sspi.md) ).

Um pacote de segurança que funciona como um pacote de autenticação e implementa a funcionalidade exigida por [*SSPI*](../secgloss/s-gly.md) é chamado de provedor de suporte de segurança/pacote de autenticação (SSP/AP).

Para obter mais informações sobre pacotes de segurança, consulte [pacotes SSP fornecidos pela Microsoft](ssp-packages-provided-by-microsoft.md). Para obter informações sobre como desenvolver SSP/APs personalizados, consulte [pacotes de segurança personalizados](custom-security-packages.md).

 

 
