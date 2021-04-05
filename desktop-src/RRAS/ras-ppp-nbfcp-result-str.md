---
title: Estrutura de RAS_PPP_NBFCP_RESULT (Rassapi. h)
description: A estrutura de resultado do NBFCP do RAS \_ PPP \_ \_ é usada para relatar o resultado de uma operação de projeção NBF (PPP NetBEUI Framer) para uma porta.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS da estrutura de RAS_PPP_NBFCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085662"
---
# <a name="ras_ppp_nbfcp_result-structure"></a><span data-ttu-id="f14bf-104">\_Estrutura de \_ resultado de NBFCP RAS PPP \_</span><span class="sxs-lookup"><span data-stu-id="f14bf-104">RAS\_PPP\_NBFCP\_RESULT structure</span></span>

<span data-ttu-id="f14bf-105">\[A estrutura de **resultado do RAS \_ PPP \_ NBFCP \_** não tem suporte no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="f14bf-105">\[The **RAS\_PPP\_NBFCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="f14bf-106">A estrutura de **\_ resultado do \_ NBFCP \_ do RAS PPP** é usada para relatar o resultado de uma operação de projeção NBF (PPP NetBEUI Framer) para uma porta.</span><span class="sxs-lookup"><span data-stu-id="f14bf-106">The **RAS\_PPP\_NBFCP\_RESULT** structure is used to report the result of a PPP NetBEUI Framer (NBF) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="f14bf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f14bf-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="f14bf-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f14bf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f14bf-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="f14bf-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="f14bf-110">Indica os resultados da operação de projeção NBF.</span><span class="sxs-lookup"><span data-stu-id="f14bf-110">Indicates the results of the NBF projection operation.</span></span> <span data-ttu-id="f14bf-111">Um valor sem \_ erro indica êxito; nesse caso, o membro **wszWksta** contém o nome do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="f14bf-111">A value of NO\_ERROR indicates success, in which case, the **wszWksta** member contains the name of the remote computer.</span></span> <span data-ttu-id="f14bf-112">Se a operação de projeção não foi bem-sucedida, **dwError** é um código de erro de Winerror. h ou Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="f14bf-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="f14bf-113">**dwNetBiosError**</span><span class="sxs-lookup"><span data-stu-id="f14bf-113">**dwNetBiosError**</span></span>
</dt> <dd>

<span data-ttu-id="f14bf-114">Ignorar este membro no servidor; Ele é relevante apenas no cliente.</span><span class="sxs-lookup"><span data-stu-id="f14bf-114">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="f14bf-115">**szName**</span><span class="sxs-lookup"><span data-stu-id="f14bf-115">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="f14bf-116">Ignorar este membro no servidor; Ele é relevante apenas no cliente.</span><span class="sxs-lookup"><span data-stu-id="f14bf-116">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="f14bf-117">**wszWksta**</span><span class="sxs-lookup"><span data-stu-id="f14bf-117">**wszWksta**</span></span>
</dt> <dd>

<span data-ttu-id="f14bf-118">Uma cadeia de caracteres Unicode terminada em nulo que especifica o nome NetBIOS da estação de trabalho do cliente RAS.</span><span class="sxs-lookup"><span data-stu-id="f14bf-118">A null-terminated Unicode string that specifies the NetBIOS name of the RAS client workstation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f14bf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f14bf-119">Requirements</span></span>



| <span data-ttu-id="f14bf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f14bf-120">Requirement</span></span> | <span data-ttu-id="f14bf-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f14bf-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f14bf-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f14bf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f14bf-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f14bf-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f14bf-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f14bf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f14bf-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f14bf-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f14bf-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f14bf-126">End of client support</span></span><br/>    | <span data-ttu-id="f14bf-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f14bf-127">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="f14bf-128">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f14bf-128">End of server support</span></span><br/>    | <span data-ttu-id="f14bf-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f14bf-129">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="f14bf-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f14bf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f14bf-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f14bf-131"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f14bf-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f14bf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14bf-133">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="f14bf-133">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="f14bf-134">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="f14bf-134">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="f14bf-135">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f14bf-135">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="f14bf-136">**\_resultado da \_ projeção do RAS PPP \_**</span><span class="sxs-lookup"><span data-stu-id="f14bf-136">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="f14bf-137">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="f14bf-137">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





