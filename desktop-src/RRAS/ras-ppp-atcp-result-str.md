---
title: Estrutura de RAS_PPP_ATCP_RESULT (Rassapi. h)
description: A estrutura de resultados do ATCP do RAS \_ PPP \_ \_ é usada para relatar o resultado de uma operação de projeção do protocolo AppleTalk para uma porta.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS da estrutura de RAS_PPP_ATCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918555"
---
# <a name="ras_ppp_atcp_result-structure"></a><span data-ttu-id="8296b-104">\_Estrutura de \_ resultados do ATCP do RAS PPP \_</span><span class="sxs-lookup"><span data-stu-id="8296b-104">RAS\_PPP\_ATCP\_RESULT structure</span></span>

<span data-ttu-id="8296b-105">\[Não há suporte para a estrutura de **\_ resultados do \_ ATCP \_ do protocolo RAS** no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="8296b-105">\[The **RAS\_PPP\_ATCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="8296b-106">A estrutura de **\_ resultados do \_ ATCP \_ do RAS PPP** é usada para relatar o resultado de uma operação de projeção do protocolo AppleTalk para uma porta.</span><span class="sxs-lookup"><span data-stu-id="8296b-106">The **RAS\_PPP\_ATCP\_RESULT** structure is used to report the result of an AppleTalk protocol projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="8296b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8296b-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="8296b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8296b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8296b-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="8296b-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="8296b-110">Especifica um valor que indica os resultados da operação de projeção do AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="8296b-110">Specifies a value that indicates the results of the AppleTalk projection operation.</span></span> <span data-ttu-id="8296b-111">Um valor sem \_ erro indica êxito; nesse caso, o membro **wszAddress** é válido.</span><span class="sxs-lookup"><span data-stu-id="8296b-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="8296b-112">Se a operação de projeção não for bem-sucedida, **dwError** será um código de erro de Winerror. h ou Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="8296b-112">If the projection operation is not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="8296b-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="8296b-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="8296b-114">Especifica uma cadeia de caracteres Unicode terminada em nulo que especifica o endereço IP atribuído ao cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="8296b-114">Specifies a null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8296b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8296b-115">Requirements</span></span>



| <span data-ttu-id="8296b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8296b-116">Requirement</span></span> | <span data-ttu-id="8296b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8296b-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8296b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8296b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8296b-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8296b-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8296b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8296b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8296b-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8296b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8296b-122">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8296b-122">End of client support</span></span><br/>    | <span data-ttu-id="8296b-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8296b-123">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="8296b-124">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="8296b-124">End of server support</span></span><br/>    | <span data-ttu-id="8296b-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8296b-125">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="8296b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8296b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8296b-127"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8296b-127"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8296b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8296b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8296b-129">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="8296b-129">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="8296b-130">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="8296b-130">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="8296b-131">**\_resultado da \_ projeção do RAS PPP \_**</span><span class="sxs-lookup"><span data-stu-id="8296b-131">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





