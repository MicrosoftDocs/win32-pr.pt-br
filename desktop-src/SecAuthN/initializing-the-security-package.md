---
description: Lista e explica as etapas necessárias para inicializar um pacote de segurança.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Inicializando o pacote de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091387"
---
# <a name="initializing-the-security-package"></a>Inicializando o pacote de segurança

Essas etapas são necessárias antes de usar SSPI:

1.  A função de inicialização deve ser chamada para obter o endereço da tabela de funções de segurança.

    O cliente e o servidor chamam [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) para um ponteiro para uma tabela de expedição [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) . Esta tabela contém ponteiros para funções de retorno de chamada declaradas em SSPI. h. Esses ponteiros fornecem acesso às implementações da DLL das várias funções SSPI.

2.  As informações devem ser obtidas sobre os pacotes de segurança com suporte.

    Embora a maioria dos aplicativos use pacotes de segurança que dão suporte a recursos padrão ou comuns, os pacotes de segurança podem ter recursos exclusivos de interesse para o aplicativo. Um aplicativo que precisa de recursos especiais pode usar um pacote que oferece esses recursos. Para obter mais informações, consulte [obtendo informações sobre pacotes de segurança](getting-information-about-security-packages.md).

Neste ponto, o aplicativo inicializou com êxito um SSP e escolheu um pacote de segurança com recursos suficientes.

O pacote [*Negotiate*](../secgloss/n-gly.md) pode ser usado em que contrato entre o cliente e o servidor sobre qual [*pacote de segurança*](../secgloss/s-gly.md) usar é feito nos bastidores. Se o pacote Negotiate não for usado, o cliente e o servidor deverão concordar com o pacote de segurança específico a ser usado antes de executar as etapas de configuração acima.

 

 
