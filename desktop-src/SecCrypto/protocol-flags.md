---
description: Constantes predefinidas para protocolos de criptografia. Esses valores são definidos em Wincrypt. h.
ms.assetid: 61dc0eff-2033-464a-a558-1798a92d48a2
title: Sinalizadores de protocolo (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25804763e407ff2a12e5657878e343f483d353e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922354"
---
# <a name="protocol-flags"></a><span data-ttu-id="03988-104">Sinalizadores de protocolo</span><span class="sxs-lookup"><span data-stu-id="03988-104">Protocol Flags</span></span>

<span data-ttu-id="03988-105">A seguir estão constantes predefinidas para protocolos de criptografia.</span><span class="sxs-lookup"><span data-stu-id="03988-105">The following are predefined constants for cryptography protocols.</span></span> <span data-ttu-id="03988-106">Esses valores são definidos em Wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="03988-106">These values are defined in Wincrypt.h.</span></span>



| <span data-ttu-id="03988-107">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="03988-107">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="03988-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="03988-108">Description</span></span>                                                           |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="CRYPT_FLAG_IPSEC"></span><span id="crypt_flag_ipsec"></span><dl> <span data-ttu-id="03988-109"><dt>**Cript \_ SINALIZADOR \_**</dt> de <dt>0x0010</dt> IPSec</span><span class="sxs-lookup"><span data-stu-id="03988-109"><dt>**CRYPT\_FLAG\_IPSEC**</dt> <dt>0x0010</dt></span></span> </dl>       | <span data-ttu-id="03988-110">Protocolo IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="03988-110">Internet protocol security (IPsec) protocol.</span></span><br/>               |
| <span id="CRYPT_FLAG_PCT1"></span><span id="crypt_flag_pct1"></span><dl> <span data-ttu-id="03988-111"><dt>**Cript \_ SINALIZADOR \_ PCT1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="03988-111"><dt>**CRYPT\_FLAG\_PCT1**</dt> <dt>0x0001</dt></span></span> </dl>          | <span data-ttu-id="03988-112">Protocolo de transporte de comunicações privada (PCT) versão 1.</span><span class="sxs-lookup"><span data-stu-id="03988-112">Private communications transport (PCT) version 1 protocol.</span></span><br/> |
| <span id="CRYPT_FLAG_SIGNING"></span><span id="crypt_flag_signing"></span><dl> <span data-ttu-id="03988-113"><dt>**Cript \_ SINALIZAr \_**</dt> <dt>0x0020</dt> de assinatura</span><span class="sxs-lookup"><span data-stu-id="03988-113"><dt>**CRYPT\_FLAG\_SIGNING**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="03988-114">Protocolo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="03988-114">Signing protocol.</span></span><br/>                                          |
| <span id="CRYPT_FLAG_SSL2"></span><span id="crypt_flag_ssl2"></span><dl> <span data-ttu-id="03988-115"><dt>**Cript \_ SINALIZADOR \_ SSL2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="03988-115"><dt>**CRYPT\_FLAG\_SSL2**</dt> <dt>0x0002</dt></span></span> </dl>          | <span data-ttu-id="03988-116">Protocolo SSL versão 2 (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="03988-116">Secure sockets layer (SSL) version 2 protocol.</span></span><br/>             |
| <span id="CRYPT_FLAG_SSL3"></span><span id="crypt_flag_ssl3"></span><dl> <span data-ttu-id="03988-117"><dt>**Cript \_ SINALIZADOR \_ SSL3**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="03988-117"><dt>**CRYPT\_FLAG\_SSL3**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="03988-118">Protocolo SSL versão 3.</span><span class="sxs-lookup"><span data-stu-id="03988-118">SSL version 3 protocol.</span></span><br/>                                    |
| <span id="CRYPT_FLAG_TLS1"></span><span id="crypt_flag_tls1"></span><dl> <span data-ttu-id="03988-119"><dt>**Cript \_ SINALIZADOR \_ TLS1**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="03988-119"><dt>**CRYPT\_FLAG\_TLS1**</dt> <dt>0x0008</dt></span></span> </dl>          | <span data-ttu-id="03988-120">Protocolo TLS da versão 1.</span><span class="sxs-lookup"><span data-stu-id="03988-120">Transport layer security (TLS) version 1 protocol.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="03988-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03988-121">Requirements</span></span>



| <span data-ttu-id="03988-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="03988-122">Requirement</span></span> | <span data-ttu-id="03988-123">Valor</span><span class="sxs-lookup"><span data-stu-id="03988-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03988-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03988-124">Minimum supported client</span></span><br/> | <span data-ttu-id="03988-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="03988-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="03988-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03988-126">Minimum supported server</span></span><br/> | <span data-ttu-id="03988-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03988-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03988-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03988-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="03988-129"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="03988-129"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03988-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="03988-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03988-131">**PROV \_ ENUMALGS \_ ex**</span><span class="sxs-lookup"><span data-stu-id="03988-131">**PROV\_ENUMALGS\_EX**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex)
</dt> </dl>

 

 




