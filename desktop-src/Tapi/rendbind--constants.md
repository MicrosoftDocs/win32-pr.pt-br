---
description: 'As constantes RENDBIND são sinalizadores usadas pelo método ITDirectory:: BIND para indicar os tipos de autenticação fornecidos.'
ms.assetid: 27bcf36a-1826-4603-9821-22fcc5c1e186
title: Constantes de RENDBIND_ (rend. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badd2a48b2ae0632e317522533c664d4f74a6c77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779301"
---
# <a name="rendbind_-constants"></a><span data-ttu-id="24b00-103">\_Constantes RENDBIND</span><span class="sxs-lookup"><span data-stu-id="24b00-103">RENDBIND\_ Constants</span></span>

<span data-ttu-id="24b00-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="24b00-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="24b00-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="24b00-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="24b00-106">As constantes RENDBIND são sinalizadores usadas pelo método [**ITDirectory:: bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) para indicar os tipos de autenticação fornecidos.</span><span class="sxs-lookup"><span data-stu-id="24b00-106">The RENDBIND constants are flags used by the [**ITDirectory::Bind**](/windows/desktop/api/Rend/nf-rend-itdirectory-bind) method to indicate types of authentication supplied.</span></span>

<dl> <dt>

<span data-ttu-id="24b00-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND \_ autenticar**</span><span class="sxs-lookup"><span data-stu-id="24b00-107"><span id="RENDBIND_AUTHENTICATE"></span><span id="rendbind_authenticate"></span>**RENDBIND\_AUTHENTICATE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="24b00-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="24b00-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="24b00-109">Autenticar usuário.</span><span class="sxs-lookup"><span data-stu-id="24b00-109">Authenticate user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24b00-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND \_ DEFAULTdomainname**</span><span class="sxs-lookup"><span data-stu-id="24b00-110"><span id="RENDBIND_DEFAULTDOMAINNAME"></span><span id="rendbind_defaultdomainname"></span>**RENDBIND\_DEFAULTDOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="24b00-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="24b00-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="24b00-112">Use o nome de domínio padrão.</span><span class="sxs-lookup"><span data-stu-id="24b00-112">Use default domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24b00-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND \_ DEFAULTusername**</span><span class="sxs-lookup"><span data-stu-id="24b00-113"><span id="RENDBIND_DEFAULTUSERNAME"></span><span id="rendbind_defaultusername"></span>**RENDBIND\_DEFAULTUSERNAME**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="24b00-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="24b00-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="24b00-115">Use o nome de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="24b00-115">Use default user name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24b00-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND \_ DEFAULTpassword**</span><span class="sxs-lookup"><span data-stu-id="24b00-116"><span id="RENDBIND_DEFAULTPASSWORD"></span><span id="rendbind_defaultpassword"></span>**RENDBIND\_DEFAULTPASSWORD**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="24b00-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="24b00-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="24b00-118">Use a senha padrão.</span><span class="sxs-lookup"><span data-stu-id="24b00-118">Use default password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="24b00-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND \_ DEFAULTcredentials**</span><span class="sxs-lookup"><span data-stu-id="24b00-119"><span id="RENDBIND_DEFAULTCREDENTIALS"></span><span id="rendbind_defaultcredentials"></span>**RENDBIND\_DEFAULTCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="24b00-120">0x0000000e</span><span class="sxs-lookup"><span data-stu-id="24b00-120">0x0000000e</span></span>
</dt> <dt>



<span data-ttu-id="24b00-121">Os três vinculantes anteriores juntos para sua conveniência.</span><span class="sxs-lookup"><span data-stu-id="24b00-121">The previous three ORed together for convenience.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24b00-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24b00-122">Requirements</span></span>



| <span data-ttu-id="24b00-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b00-123">Requirement</span></span> | <span data-ttu-id="24b00-124">Valor</span><span class="sxs-lookup"><span data-stu-id="24b00-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="24b00-125">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="24b00-125">TAPI version</span></span><br/> | <span data-ttu-id="24b00-126">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="24b00-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="24b00-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24b00-127">Header</span></span><br/>       | <dl> <span data-ttu-id="24b00-128"><dt>Rend. h</dt></span><span class="sxs-lookup"><span data-stu-id="24b00-128"><dt>Rend.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b00-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="24b00-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b00-130">**ITDirectory**</span><span class="sxs-lookup"><span data-stu-id="24b00-130">**ITDirectory**</span></span>](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[<span data-ttu-id="24b00-131">**ITDirectory:: bind**</span><span class="sxs-lookup"><span data-stu-id="24b00-131">**ITDirectory::Bind**</span></span>](/windows/desktop/api/Rend/nf-rend-itdirectory-bind)
</dt> </dl>

 

 




