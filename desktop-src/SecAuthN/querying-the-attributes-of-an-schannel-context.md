---
description: Fornece informações específicas do Schannel sobre um contexto de segurança.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Consultando os atributos de um contexto Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089938"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a><span data-ttu-id="cc25c-103">Consultando os atributos de um contexto Schannel</span><span class="sxs-lookup"><span data-stu-id="cc25c-103">Querying the Attributes of an Schannel Context</span></span>

<span data-ttu-id="cc25c-104">A função [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) fornece informações específicas do Schannel sobre um [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cc25c-104">The [**QueryContextAttributes (Schannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) function provides Schannel-specific information about a [*security context*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="cc25c-105">A maioria das informações é especificada originalmente quando o contexto é criado usando a função [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) ou servidor [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) do cliente.</span><span class="sxs-lookup"><span data-stu-id="cc25c-105">Most of the information is originally specified when the context is created by using the client [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) or server [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) function.</span></span> <span data-ttu-id="cc25c-106">Algumas informações são especificadas ao obter um identificador para a credencial usada para criar o contexto.</span><span class="sxs-lookup"><span data-stu-id="cc25c-106">Some information is specified when obtaining a handle to the credential used to create the context.</span></span> <span data-ttu-id="cc25c-107">Para obter mais informações, consulte [obtendo credenciais Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="cc25c-107">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
