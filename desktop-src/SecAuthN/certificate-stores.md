---
description: Os certificados de cliente e de servidor devem ser armazenados em um repositório de certificados acessível pelo processo do aplicativo.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Repositórios de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010773"
---
# <a name="certificate-stores"></a><span data-ttu-id="86011-103">Repositórios de certificados</span><span class="sxs-lookup"><span data-stu-id="86011-103">Certificate Stores</span></span>

<span data-ttu-id="86011-104">Os certificados de [*cliente*](/windows/desktop/SecGloss/c-gly) e de [*servidor*](/windows/desktop/SecGloss/s-gly) devem ser armazenados em um [*repositório de certificados*](/windows/desktop/SecGloss/c-gly) acessível pelo processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="86011-104">Both [*client*](/windows/desktop/SecGloss/c-gly) and [*server certificates*](/windows/desktop/SecGloss/s-gly) must be stored in a [*certificate store*](/windows/desktop/SecGloss/c-gly) accessible by the application process.</span></span> <span data-ttu-id="86011-105">Normalmente, essa é a minha loja, também conhecida como o armazenamento pessoal.</span><span class="sxs-lookup"><span data-stu-id="86011-105">Typically, this is the My store, also known as the personal store.</span></span> <span data-ttu-id="86011-106">Aplicativos cliente, como o Internet Explorer, normalmente usam o repositório My do usuário atual, enquanto os servidores como o Serviços de Informações da Internet (IIS) usam o meu repositório do sistema do computador local.</span><span class="sxs-lookup"><span data-stu-id="86011-106">Client applications such as Internet Explorer normally use the My store of the current user while servers such as Internet Information Services (IIS) use the system My store of the local computer.</span></span>

<span data-ttu-id="86011-107">O repositório raiz e o armazenamento de [*autoridade de certificação*](/windows/desktop/SecGloss/c-gly) (CA) são usados quando o Schannel ou um aplicativo cria uma cadeia de certificados para ser enviada ao computador remoto.</span><span class="sxs-lookup"><span data-stu-id="86011-107">The Root store and the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) store are used when Schannel or an application builds a certificate chain to be sent to the remote computer.</span></span> <span data-ttu-id="86011-108">Esses armazenamentos são usados para validar uma cadeia de certificados recebida.</span><span class="sxs-lookup"><span data-stu-id="86011-108">These stores are used to validate a received certificate chain.</span></span> <span data-ttu-id="86011-109">Para obter mais informações, consulte [executando a autenticação usando Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="86011-109">For more information, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
