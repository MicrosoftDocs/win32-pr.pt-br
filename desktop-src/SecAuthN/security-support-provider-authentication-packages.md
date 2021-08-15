---
description: O Windows operacional dá suporte à autenticação usando pacotes de segurança que funcionam como provedores de suporte de segurança e como pacotes de autenticação.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Provedor de suporte de segurança/pacotes de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62f634d0571eab43652485f8ca1313f78fd157ca202d5d78369552db648de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918335"
---
# <a name="security-support-providerauthentication-packages"></a>Provedor de suporte de segurança/pacotes de autenticação

O Windows operacional dá suporte [](../secgloss/s-gly.md) à autenticação usando pacotes de segurança que funcionam como provedores de suporte [*de segurança*](../secgloss/s-gly.md) e como pacotes [*de autenticação*](../secgloss/a-gly.md). Os pacotes de segurança fornecem os serviços de suporte do processo de logon de um pacote de autenticação do Windows e também fornecem serviços de autenticação para aplicativos implementando um conjunto de funções mapeadas para a SSPI [(Interface](sspi.md) do Provedor de Suporte de Segurança).

Um pacote de segurança que funciona como um pacote de autenticação e implementa a funcionalidade exigida pelo [*SSPI*](../secgloss/s-gly.md) é chamado de SSP/AP (provedor de suporte de segurança).

Para obter mais informações sobre pacotes de segurança, consulte [Pacotes SSP fornecidos pela Microsoft.](ssp-packages-provided-by-microsoft.md) Para obter informações sobre como desenvolver SSP/APs personalizados, consulte [Pacotes de segurança personalizados.](custom-security-packages.md)

 

 
