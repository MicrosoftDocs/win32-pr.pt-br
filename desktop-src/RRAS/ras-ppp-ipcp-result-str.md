---
title: Estrutura de RAS_PPP_IPCP_RESULT (Rassapi. h)
description: A \_ estrutura de resultado do IPCP PPP de Ras \_ \_ é usada para relatar o resultado de uma operação de projeção de protocolo IP (PPP Internet Protocol) para uma porta.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS da estrutura de RAS_PPP_IPCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499408"
---
# <a name="ras_ppp_ipcp_result-structure"></a><span data-ttu-id="92b01-104">\_Estrutura de \_ resultado do IPCP de Ras PPP \_</span><span class="sxs-lookup"><span data-stu-id="92b01-104">RAS\_PPP\_IPCP\_RESULT structure</span></span>

<span data-ttu-id="92b01-105">\[A estrutura de **\_ resultado do protocolo \_ IPCP \_ PPP** não tem suporte no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="92b01-105">\[The **RAS\_PPP\_IPCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="92b01-106">A estrutura de **\_ \_ \_ resultado do IPCP PPP de Ras** é usada para relatar o resultado de uma operação de projeção de protocolo IP (PPP Internet Protocol) para uma porta.</span><span class="sxs-lookup"><span data-stu-id="92b01-106">The **RAS\_PPP\_IPCP\_RESULT** structure is used to report the result of a PPP Internet Protocol (IP) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b01-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92b01-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="92b01-108">Membros</span><span class="sxs-lookup"><span data-stu-id="92b01-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="92b01-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="92b01-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="92b01-110">Indica os resultados da operação de projeção de IP.</span><span class="sxs-lookup"><span data-stu-id="92b01-110">Indicates the results of the IP projection operation.</span></span> <span data-ttu-id="92b01-111">Um valor sem \_ erro indica êxito; nesse caso, o membro **wszAddress** é válido.</span><span class="sxs-lookup"><span data-stu-id="92b01-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="92b01-112">Se a operação de projeção não foi bem-sucedida, **dwError** é um código de erro de Winerror. h ou Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="92b01-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="92b01-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="92b01-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="92b01-114">Uma cadeia de caracteres Unicode terminada em nulo que especifica o endereço IP atribuído ao cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="92b01-114">A null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span> <span data-ttu-id="92b01-115">Essa cadeia de caracteres tem a forma \*um ***.** _b_* _._ *_c_*_._ \* _d_.</span><span class="sxs-lookup"><span data-stu-id="92b01-115">This string has the form *a\***.**_b_*_._*_c_*_._\*_d_.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92b01-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92b01-116">Requirements</span></span>



| <span data-ttu-id="92b01-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b01-117">Requirement</span></span> | <span data-ttu-id="92b01-118">Valor</span><span class="sxs-lookup"><span data-stu-id="92b01-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92b01-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92b01-119">Minimum supported client</span></span><br/> | <span data-ttu-id="92b01-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92b01-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="92b01-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92b01-121">Minimum supported server</span></span><br/> | <span data-ttu-id="92b01-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="92b01-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="92b01-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="92b01-123">End of client support</span></span><br/>    | <span data-ttu-id="92b01-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="92b01-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="92b01-125">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="92b01-125">End of server support</span></span><br/>    | <span data-ttu-id="92b01-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92b01-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="92b01-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92b01-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="92b01-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b01-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b01-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="92b01-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b01-130">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="92b01-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="92b01-131">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="92b01-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="92b01-132">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="92b01-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="92b01-133">**\_resultado da \_ projeção do RAS PPP \_**</span><span class="sxs-lookup"><span data-stu-id="92b01-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="92b01-134">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="92b01-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





