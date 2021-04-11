---
title: Estrutura de RAS_PPP_IPXCP_RESULT (Rassapi. h)
description: A \_ estrutura de resultados do protocolo PPP do RAS \_ \_ é usada para relatar o resultado de uma operação de projeção de intercâmbio de pacotes de rede PPP (IPX) para uma porta.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS da estrutura de RAS_PPP_IPXCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009444"
---
# <a name="ras_ppp_ipxcp_result-structure"></a><span data-ttu-id="fc300-104">Estrutura de resultados do protocolo RAS \_ PPP \_ \_</span><span class="sxs-lookup"><span data-stu-id="fc300-104">RAS\_PPP\_IPXCP\_RESULT structure</span></span>

<span data-ttu-id="fc300-105">\[Não há suporte para a estrutura de **\_ \_ \_ resultado do protocolo RAS PPP** no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="fc300-105">\[The **RAS\_PPP\_IPXCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="fc300-106">A estrutura de **\_ \_ \_ resultados do protocolo PPP do RAS** é usada para relatar o resultado de uma operação de projeção de intercâmbio de pacotes de rede PPP (IPX) para uma porta.</span><span class="sxs-lookup"><span data-stu-id="fc300-106">The **RAS\_PPP\_IPXCP\_RESULT** structure is used to report the result of a PPP Internetwork Packet Exchange (IPX) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc300-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc300-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="fc300-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fc300-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc300-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="fc300-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="fc300-110">Indica os resultados da operação de projeção IPX.</span><span class="sxs-lookup"><span data-stu-id="fc300-110">Indicates the results of the IPX projection operation.</span></span> <span data-ttu-id="fc300-111">Um valor sem \_ erro indica êxito; nesse caso, o membro **wszAddress** é válido.</span><span class="sxs-lookup"><span data-stu-id="fc300-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="fc300-112">Se a operação de projeção não foi bem-sucedida, **dwError** é um código de erro de Winerror. h ou Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="fc300-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="fc300-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="fc300-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="fc300-114">Uma cadeia de caracteres Unicode terminada em nulo que especifica o Endereço IPX atribuído ao cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="fc300-114">A null-terminated Unicode string that specifies the IPX address assigned to the remote client.</span></span> <span data-ttu-id="fc300-115">Essa cadeia de caracteres tem o \* NET \***.** formulário de _nó_ .</span><span class="sxs-lookup"><span data-stu-id="fc300-115">This string has the \*net\***.**_node_ form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc300-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc300-116">Requirements</span></span>



| <span data-ttu-id="fc300-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc300-117">Requirement</span></span> | <span data-ttu-id="fc300-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fc300-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc300-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc300-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc300-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc300-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fc300-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc300-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc300-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc300-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fc300-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fc300-123">End of client support</span></span><br/>    | <span data-ttu-id="fc300-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc300-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="fc300-125">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="fc300-125">End of server support</span></span><br/>    | <span data-ttu-id="fc300-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fc300-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="fc300-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc300-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc300-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc300-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc300-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc300-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc300-130">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="fc300-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="fc300-131">Estruturas de administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="fc300-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="fc300-132">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="fc300-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="fc300-133">**\_resultado da \_ projeção do RAS PPP \_**</span><span class="sxs-lookup"><span data-stu-id="fc300-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="fc300-134">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="fc300-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





