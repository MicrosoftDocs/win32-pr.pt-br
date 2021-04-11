---
description: Fornece informações específicas do Schannel sobre uma credencial.
ms.assetid: 0c357996-b85a-4231-b258-40b35ab83ae2
title: Consultando os atributos de uma credencial Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc63ccc358561dea95cb1273e1367e7fbb39d390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169369"
---
# <a name="querying-the-attributes-of-an-schannel-credential"></a><span data-ttu-id="b1c0b-103">Consultando os atributos de uma credencial Schannel</span><span class="sxs-lookup"><span data-stu-id="b1c0b-103">Querying the Attributes of an Schannel Credential</span></span>

<span data-ttu-id="b1c0b-104">A função [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) fornece informações específicas do Schannel sobre uma credencial.</span><span class="sxs-lookup"><span data-stu-id="b1c0b-104">The [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) function provides Schannel-specific information about a credential.</span></span> <span data-ttu-id="b1c0b-105">Essas informações são especificadas originalmente quando a credencial é criada.</span><span class="sxs-lookup"><span data-stu-id="b1c0b-105">This information is originally specified when the credential is created.</span></span> <span data-ttu-id="b1c0b-106">Para obter mais informações, consulte [obtendo credenciais Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="b1c0b-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span> <span data-ttu-id="b1c0b-107">As informações relatadas por essa função são válidas para quaisquer conexões ([*contextos de segurança*](../secgloss/s-gly.md)) criadas usando a credencial especificada.</span><span class="sxs-lookup"><span data-stu-id="b1c0b-107">The information reported by this function is valid for any connections ([*security contexts*](../secgloss/s-gly.md)) created by using the specified credential.</span></span>

 

 
