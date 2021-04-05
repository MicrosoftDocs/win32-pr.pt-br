---
title: Função FreeCountedString (NapUtil. h)
description: Libera uma estrutura de dados contada.
ms.assetid: d080d247-9339-474b-866e-b412e82dd35f
keywords:
- Função FreeCountedString NAP
topic_type:
- apiref
api_name:
- FreeCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f732a069d19d6b8948854bd1fe2e23be070aa23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918010"
---
# <a name="freecountedstring-function"></a><span data-ttu-id="5c3e6-104">Função FreeCountedString</span><span class="sxs-lookup"><span data-stu-id="5c3e6-104">FreeCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="5c3e6-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="5c3e6-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5c3e6-106">A função **FreeCountedString** libera uma estrutura de dados de [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .</span><span class="sxs-lookup"><span data-stu-id="5c3e6-106">The **FreeCountedString** function frees a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c3e6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c3e6-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeCountedString(
  _In_ CountedString *countedString
);
```



## <a name="parameters"></a><span data-ttu-id="5c3e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c3e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c3e6-109">*contado* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c3e6-109">*countedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c3e6-110">Um ponteiro para a estrutura de dados [**contada**](/windows/win32/api/naptypes/ns-naptypes-countedstring) como livre.</span><span class="sxs-lookup"><span data-stu-id="5c3e6-110">A pointer to the [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c3e6-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c3e6-111">Remarks</span></span>

<span data-ttu-id="5c3e6-112">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="5c3e6-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="5c3e6-113">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="5c3e6-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="5c3e6-114">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="5c3e6-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="5c3e6-115">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="5c3e6-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="5c3e6-116">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="5c3e6-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c3e6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c3e6-117">Requirements</span></span>



| <span data-ttu-id="5c3e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c3e6-118">Requirement</span></span> | <span data-ttu-id="5c3e6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5c3e6-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5c3e6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c3e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5c3e6-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c3e6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5c3e6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c3e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5c3e6-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c3e6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5c3e6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c3e6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c3e6-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c3e6-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="5c3e6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5c3e6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c3e6-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c3e6-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c3e6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c3e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c3e6-129">**AllocCountedString**</span><span class="sxs-lookup"><span data-stu-id="5c3e6-129">**AllocCountedString**</span></span>](alloccountedstring-func.md)
</dt> </dl>

 

 





