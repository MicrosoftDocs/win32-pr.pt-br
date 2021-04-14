---
title: Função FreeNetworkSoH (NapUtil. h)
description: Libera uma estrutura de dados NetworkSoH.
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- Função FreeNetworkSoH NAP
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ea2b72011332939aa0c814203d0004949c8341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455725"
---
# <a name="freenetworksoh-function"></a><span data-ttu-id="513bc-104">Função FreeNetworkSoH</span><span class="sxs-lookup"><span data-stu-id="513bc-104">FreeNetworkSoH function</span></span>

> [!Note]  
> <span data-ttu-id="513bc-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="513bc-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="513bc-106">A função **FreeNetworkSoH** libera uma estrutura de dados [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) .</span><span class="sxs-lookup"><span data-stu-id="513bc-106">The **FreeNetworkSoH** function frees a [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="513bc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="513bc-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a><span data-ttu-id="513bc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="513bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="513bc-109">*networkSoh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="513bc-109">*networkSoh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="513bc-110">Um ponteiro para a estrutura de dados [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) para liberar.</span><span class="sxs-lookup"><span data-stu-id="513bc-110">A pointer to the [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="513bc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="513bc-111">Remarks</span></span>

<span data-ttu-id="513bc-112">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="513bc-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="513bc-113">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="513bc-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="513bc-114">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="513bc-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="513bc-115">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="513bc-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="513bc-116">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="513bc-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="513bc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="513bc-117">Requirements</span></span>



| <span data-ttu-id="513bc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="513bc-118">Requirement</span></span> | <span data-ttu-id="513bc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="513bc-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="513bc-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="513bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="513bc-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="513bc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="513bc-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="513bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="513bc-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="513bc-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="513bc-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="513bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="513bc-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="513bc-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="513bc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="513bc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="513bc-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="513bc-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





