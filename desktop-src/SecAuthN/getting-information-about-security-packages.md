---
description: Quando um cliente é iniciado, ele seleciona um pacote de segurança para suas transações com um servidor e, em seguida, entra em contato com esse servidor. Um servidor seleciona um ou mais pacotes de segurança e aguarda uma conexão de cliente.
ms.assetid: eaed162b-ef07-4295-93d9-6be91232a82e
title: Obtendo informações sobre pacotes de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca690575ff7f46ef5a5b1d971b1ab9fdd91f95e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090758"
---
# <a name="getting-information-about-security-packages"></a>Obtendo informações sobre pacotes de segurança

Quando um cliente é iniciado, ele seleciona um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) para suas transações com um servidor e, em seguida, entra em contato com esse servidor. Um servidor seleciona um ou mais pacotes de segurança e aguarda uma conexão de cliente.

Para obter informações específicas sobre os pacotes de segurança SSPI disponíveis com um SSP específico, a função [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) pode ser chamada para recuperar uma estrutura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) .

Para recuperar a estrutura de saída, o chamador passa para a função o endereço de um ponteiro para o tipo da estrutura de retorno. A função aloca memória e retorna os dados para o chamador atribuindo o endereço do buffer de dados de retorno ao argumento. A Convenção SSPI é que a função aloca memória para a estrutura e o aplicativo de chamada libera essa memória usando [**FreeContextBuffer**](/windows/desktop/api/Sspi/nf-sspi-freecontextbuffer).

Chamar a função [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa) recupera os atributos de um [*pacote de segurança*](/windows/desktop/SecGloss/s-gly). Tanto o servidor quanto o cliente podem chamar a função **QuerySecurityPackageInfo** para obter o comprimento máximo do token de segurança do membro **CbMaxToken** da estrutura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) . Para obter um exemplo, consulte a chamada para a função **QuerySecurityPackageInfo** mostrada em [usando SSPI com um servidor do Windows Sockets](using-sspi-with-a-windows-sockets-server.md).

Para obter mais informações sobre as funções de pacote, consulte [Gerenciamento de pacotes](authentication-functions.md).

 

 
