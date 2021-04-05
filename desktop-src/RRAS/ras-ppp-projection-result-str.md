---
title: Estrutura de RAS_PPP_PROJECTION_RESULT (Rassapi. h)
description: A \_ estrutura de \_ resultados de projeção de Ras PPP \_ é usada para relatar os resultados das várias operações de projeção de PPP para uma porta.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS da estrutura de RAS_PPP_PROJECTION_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644723"
---
# <a name="ras_ppp_projection_result-structure"></a><span data-ttu-id="cd5ab-104">\_Estrutura de \_ resultados da projeção do RAS PPP \_</span><span class="sxs-lookup"><span data-stu-id="cd5ab-104">RAS\_PPP\_PROJECTION\_RESULT structure</span></span>

<span data-ttu-id="cd5ab-105">\[A estrutura de **\_ \_ \_ resultados de projeção de Ras PPP** não tem suporte no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="cd5ab-105">\[The **RAS\_PPP\_PROJECTION\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="cd5ab-106">A estrutura de **\_ \_ \_ resultados de projeção de Ras PPP** é usada para relatar os resultados das várias operações de projeção de PPP para uma porta.</span><span class="sxs-lookup"><span data-stu-id="cd5ab-106">The **RAS\_PPP\_PROJECTION\_RESULT** structure is used to report the results of the various PPP projection operations for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd5ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd5ab-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a><span data-ttu-id="cd5ab-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cd5ab-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd5ab-109">**nbf**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-109">**nbf**</span></span>
</dt> <dd>

<span data-ttu-id="cd5ab-110">Uma estrutura de [**\_ resultado de \_ NBFCP \_ RAS PPP**](ras-ppp-nbfcp-result-str.md) que relata o resultado de uma operação de projeção NBF (PPP NetBEUI Framer).</span><span class="sxs-lookup"><span data-stu-id="cd5ab-110">A [**RAS\_PPP\_NBFCP\_RESULT**](ras-ppp-nbfcp-result-str.md) structure that reports the result of a PPP NetBEUI Framer (NBF) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd5ab-111">**IP**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-111">**ip**</span></span>
</dt> <dd>

<span data-ttu-id="cd5ab-112">Uma estrutura de resultado do protocolo [**\_ \_ IPCP \_ de Ras PPP**](ras-ppp-ipcp-result-str.md) que relata o resultado de uma operação de projeção de IP (PPP Internet Protocol).</span><span class="sxs-lookup"><span data-stu-id="cd5ab-112">A [**RAS\_PPP\_IPCP\_RESULT**](ras-ppp-ipcp-result-str.md) structure that reports the result of a PPP Internet Protocol (IP) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd5ab-113">**IPX**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-113">**ipx**</span></span>
</dt> <dd>

<span data-ttu-id="cd5ab-114">Uma estrutura de [**\_ \_ \_ resultados do protocolo**](ras-ppp-ipxcp-result-str.md) de rede IP do PPP do RAS que relata o resultado de uma operação de projeção de IPX (troca de pacotes de Internet) PPP.</span><span class="sxs-lookup"><span data-stu-id="cd5ab-114">A [**RAS\_PPP\_IPXCP\_RESULT**](ras-ppp-ipxcp-result-str.md) structure that reports the result of a PPP Internetwork Packet Exchange (IPX) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd5ab-115">**at**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-115">**at**</span></span>
</dt> <dd>

<span data-ttu-id="cd5ab-116">Uma estrutura de [**\_ resultados do protocolo \_ ATCP \_ do RAS**](ras-ppp-atcp-result-str.md) .</span><span class="sxs-lookup"><span data-stu-id="cd5ab-116">A [**RAS\_PPP\_ATCP\_RESULT**](ras-ppp-atcp-result-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd5ab-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd5ab-117">Remarks</span></span>

<span data-ttu-id="cd5ab-118">Essa estrutura relata os resultados da projeção para protocolos NetBEUI, TCP/IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="cd5ab-118">This structure reports the projection results for NetBEUI, TCP/IP, and IPX protocols.</span></span> <span data-ttu-id="cd5ab-119">Cada estrutura PPP tem um membro **dwError** que indica se as outras informações na estrutura são válidas.</span><span class="sxs-lookup"><span data-stu-id="cd5ab-119">Each PPP structure has a **dwError** member that indicates whether the other information in the structure is valid.</span></span> <span data-ttu-id="cd5ab-120">Se **dwError** não for um \_ erro, as outras informações serão válidas.</span><span class="sxs-lookup"><span data-stu-id="cd5ab-120">If **dwError** is NO\_ERROR, the other information is valid.</span></span> <span data-ttu-id="cd5ab-121">Se **dwError** for um dos códigos de erro em Winerror. h ou Raserror. h, as outras informações não serão válidas.</span><span class="sxs-lookup"><span data-stu-id="cd5ab-121">If **dwError** is one of the error codes in Winerror.h or Raserror.h, the other information is not valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd5ab-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd5ab-122">Requirements</span></span>



| <span data-ttu-id="cd5ab-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd5ab-123">Requirement</span></span> | <span data-ttu-id="cd5ab-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cd5ab-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd5ab-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd5ab-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cd5ab-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd5ab-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cd5ab-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd5ab-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cd5ab-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cd5ab-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd5ab-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cd5ab-129">End of client support</span></span><br/>    | <span data-ttu-id="cd5ab-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd5ab-130">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="cd5ab-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="cd5ab-131">End of server support</span></span><br/>    | <span data-ttu-id="cd5ab-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd5ab-132">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="cd5ab-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd5ab-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd5ab-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd5ab-134"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd5ab-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd5ab-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd5ab-136">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="cd5ab-136">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="cd5ab-137">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="cd5ab-137">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="cd5ab-138">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-138">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="cd5ab-139">**resultado do ATCP do RAS \_ PPP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-139">**RAS\_PPP\_ATCP\_RESULT**</span></span>](ras-ppp-atcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="cd5ab-140">**resultado do IPCP de RAS \_ PPP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-140">**RAS\_PPP\_IPCP\_RESULT**</span></span>](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="cd5ab-141">**resultado de IPXCP do RAS \_ PPP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-141">**RAS\_PPP\_IPXCP\_RESULT**</span></span>](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="cd5ab-142">**\_resultado de \_ NBFCP RAS PPP \_**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-142">**RAS\_PPP\_NBFCP\_RESULT**</span></span>](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="cd5ab-143">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="cd5ab-143">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





