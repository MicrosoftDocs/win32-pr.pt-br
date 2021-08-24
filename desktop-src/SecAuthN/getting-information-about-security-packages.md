---
description: Quando um cliente começa, ele seleciona um pacote de segurança para suas transações com um servidor e, em seguida, contata esse servidor. Um servidor seleciona um ou mais pacotes de segurança e aguarda uma conexão de cliente.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Obter informações sobre pacotes de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626b5bf53ddc9ef20f0110dc7695a7245245604ca9e11baa3cbb50b2c1bd393f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883096"
---
# <a name="getting-information-about-security-packages"></a>Obter informações sobre pacotes de segurança

Quando um cliente começa, ele seleciona um [*pacote*](/windows/desktop/SecGloss/s-gly) de segurança para suas transações com um servidor e, em seguida, contata esse servidor. Um servidor seleciona um ou mais pacotes de segurança e aguarda uma conexão de cliente.

Para obter informações específicas sobre os pacotes de segurança SSPI disponíveis com um SSP específico, a função [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) pode ser chamada para recuperar uma estrutura [**SecPkgInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)

Para recuperar a estrutura de saída, o chamador passa para a função o endereço de um ponteiro para o tipo da estrutura de retorno. A função aloca memória e retorna os dados ao chamador atribuindo o endereço do buffer de dados de retorno ao argumento . A convenção SSPI é que a função aloca memória para a estrutura e o aplicativo de chamada libera essa memória usando [**FreeContextBuffer.**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer)

Chamar a [**função QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) recupera os atributos de um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly). Tanto o servidor quanto o cliente podem chamar a função **QuerySecurityPackageInfo** para obter o comprimento máximo do token de segurança do membro **cbMaxToken** da estrutura [**SecPkgInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) Para ver um exemplo, consulte a chamada para a **função QuerySecurityPackageInfo** mostrada em [Usando SSPI com um servidor Windows Sockets.](using-sspi-with-a-windows-sockets-server.md)

Para obter mais informações sobre funções de pacote, [consulte Gerenciamento de Pacotes](authentication-functions.md).

 

 
