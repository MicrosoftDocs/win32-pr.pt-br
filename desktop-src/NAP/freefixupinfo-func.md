---
title: Função FreeFixupInfo (NapUtil. h)
description: Libera uma estrutura de dados FixupInfo.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- Função FreeFixupInfo NAP
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abf1fe07557ac786a9f0cb8e8e06a30408f6d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758603"
---
# <a name="freefixupinfo-function"></a><span data-ttu-id="97617-104">Função FreeFixupInfo</span><span class="sxs-lookup"><span data-stu-id="97617-104">FreeFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="97617-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="97617-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="97617-106">A função **FreeFixupInfo** libera uma estrutura de dados [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) .</span><span class="sxs-lookup"><span data-stu-id="97617-106">The **FreeFixupInfo** function frees a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="97617-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97617-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="97617-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97617-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97617-109">*fixupInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97617-109">*fixupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97617-110">Um ponteiro para a estrutura de dados [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) para liberar.</span><span class="sxs-lookup"><span data-stu-id="97617-110">A pointer to the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97617-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="97617-111">Remarks</span></span>

<span data-ttu-id="97617-112">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="97617-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="97617-113">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="97617-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="97617-114">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="97617-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="97617-115">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="97617-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="97617-116">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="97617-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="97617-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97617-117">Requirements</span></span>



| <span data-ttu-id="97617-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="97617-118">Requirement</span></span> | <span data-ttu-id="97617-119">Valor</span><span class="sxs-lookup"><span data-stu-id="97617-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97617-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97617-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97617-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97617-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="97617-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97617-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97617-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97617-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="97617-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97617-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97617-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="97617-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="97617-126">DLL</span><span class="sxs-lookup"><span data-stu-id="97617-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97617-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97617-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97617-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="97617-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97617-129">**AllocFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="97617-129">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
</dt> </dl>

 

 





