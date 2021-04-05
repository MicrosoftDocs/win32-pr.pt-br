---
title: Função FreeNapComponentRegistrationInfoArray (NapUtil. h)
description: Libera um número especificado de estruturas de dados NapComponentRegistrationInfo de uma matriz.
ms.assetid: 6fcb1394-04dd-4d8a-87f7-6b69b6ef29ff
keywords:
- Função FreeNapComponentRegistrationInfoArray NAP
topic_type:
- apiref
api_name:
- FreeNapComponentRegistrationInfoArray
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df823ad8086c57a6ee193bd0d58678786cfe325b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086135"
---
# <a name="freenapcomponentregistrationinfoarray-function"></a><span data-ttu-id="e87e5-104">Função FreeNapComponentRegistrationInfoArray</span><span class="sxs-lookup"><span data-stu-id="e87e5-104">FreeNapComponentRegistrationInfoArray function</span></span>

> [!Note]  
> <span data-ttu-id="e87e5-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="e87e5-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e87e5-106">A função **FreeNapComponentRegistrationInfoArray** libera um número especificado de estruturas de dados [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) de uma matriz.</span><span class="sxs-lookup"><span data-stu-id="e87e5-106">The **FreeNapComponentRegistrationInfoArray** function frees a specified number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures from an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="e87e5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e87e5-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNapComponentRegistrationInfoArray(
  _In_ UINT16                       count,
  _In_ NapComponentRegistrationInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="e87e5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e87e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e87e5-109">*contagem* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="e87e5-109">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e87e5-110">O número de estruturas [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) em *informações* a serem liberadas.</span><span class="sxs-lookup"><span data-stu-id="e87e5-110">The number of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures in *info* to free.</span></span>

</dd> <dt>

<span data-ttu-id="e87e5-111">*informações* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e87e5-111">*info* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e87e5-112">Um ponteiro para uma matriz de estruturas de dados [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) a serem liberadas.</span><span class="sxs-lookup"><span data-stu-id="e87e5-112">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structures to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e87e5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e87e5-113">Remarks</span></span>

<span data-ttu-id="e87e5-114">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="e87e5-114">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="e87e5-115">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="e87e5-115">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="e87e5-116">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="e87e5-116">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="e87e5-117">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="e87e5-117">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="e87e5-118">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="e87e5-118">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="e87e5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e87e5-119">Requirements</span></span>



| <span data-ttu-id="e87e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e87e5-120">Requirement</span></span> | <span data-ttu-id="e87e5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e87e5-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e87e5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e87e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e87e5-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e87e5-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e87e5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e87e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e87e5-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e87e5-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e87e5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e87e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e87e5-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="e87e5-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="e87e5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e87e5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e87e5-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e87e5-129"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





