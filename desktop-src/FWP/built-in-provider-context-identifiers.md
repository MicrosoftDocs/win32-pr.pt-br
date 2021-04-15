---
title: Identificadores de contexto do provedor interno (Fwpmu. h)
description: Contextos de provedor interno identificam as políticas padrão a serem usadas com soquetes de segurança.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454609"
---
# <a name="built-in-provider-context-identifiers"></a><span data-ttu-id="27d42-103">Identificadores de contexto do provedor interno</span><span class="sxs-lookup"><span data-stu-id="27d42-103">Built-in Provider Context Identifiers</span></span>

<span data-ttu-id="27d42-104">Os identificadores para os contextos de provedor que são internos à WFP (Windows Filtering Platform) são representados por um GUID.</span><span class="sxs-lookup"><span data-stu-id="27d42-104">The identifiers for the provider contexts that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="27d42-105">Esses contextos de provedor internos identificam as políticas padrão a serem usadas com soquetes seguros.</span><span class="sxs-lookup"><span data-stu-id="27d42-105">These built-in provider contexts identify the default policies to use with secure sockets.</span></span>

<span data-ttu-id="27d42-106">Esses identificadores são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="27d42-106">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="27d42-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM \_ de \_ \_ soquete seguro do contexto do \_ provedor \_**</span><span class="sxs-lookup"><span data-stu-id="27d42-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="27d42-108">Política padrão de modo principal de AuthIP (protocolo Authenticated IP) para soquetes seguros.</span><span class="sxs-lookup"><span data-stu-id="27d42-108">Authenticated Internet Protocol (AuthIP) main mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="27d42-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**contexto do provedor de FWPM \_ \_ \_ Secure \_ Socket \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="27d42-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="27d42-110">Política padrão de modo rápido do IPsec (Internet Protocol Security) para soquetes seguros.</span><span class="sxs-lookup"><span data-stu-id="27d42-110">Internet Protocol Security (IPsec) quick mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27d42-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d42-111">Requirements</span></span>



| <span data-ttu-id="27d42-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d42-112">Requirement</span></span> | <span data-ttu-id="27d42-113">Valor</span><span class="sxs-lookup"><span data-stu-id="27d42-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27d42-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27d42-114">Minimum supported client</span></span><br/> | <span data-ttu-id="27d42-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27d42-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="27d42-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27d42-116">Minimum supported server</span></span><br/> | <span data-ttu-id="27d42-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27d42-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="27d42-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27d42-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="27d42-119"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="27d42-119"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





