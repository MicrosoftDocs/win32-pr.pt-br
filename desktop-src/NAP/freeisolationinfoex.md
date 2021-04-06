---
title: Função FreeIsolationInfoEx (NapUtil. h)
description: Libera uma estrutura de dados IsolationInfoEx.
ms.assetid: 9ca0e5ae-aed9-43e9-b8f7-90f13d62ac16
keywords:
- Função FreeIsolationInfoEx NAP
topic_type:
- apiref
api_name:
- FreeIsolationInfoEx
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cf3f13f38130fe86383fee5bebe3a536ea9aad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086136"
---
# <a name="freeisolationinfoex-function"></a><span data-ttu-id="913af-104">Função FreeIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="913af-104">FreeIsolationInfoEx function</span></span>

> [!Note]  
> <span data-ttu-id="913af-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="913af-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="913af-106">A função **FreeIsolationInfoEx** libera uma estrutura de dados [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .</span><span class="sxs-lookup"><span data-stu-id="913af-106">The **FreeIsolationInfoEx** function frees an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="913af-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="913af-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeIsolationInfoEx(
  _In_ IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="913af-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="913af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913af-109">*isolationInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="913af-109">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="913af-110">Um ponteiro para a estrutura de dados [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) para liberar.</span><span class="sxs-lookup"><span data-stu-id="913af-110">A pointer to the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="913af-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="913af-111">Remarks</span></span>

<span data-ttu-id="913af-112">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="913af-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="913af-113">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="913af-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="913af-114">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="913af-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="913af-115">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="913af-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="913af-116">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="913af-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="913af-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="913af-117">Requirements</span></span>



| <span data-ttu-id="913af-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="913af-118">Requirement</span></span> | <span data-ttu-id="913af-119">Valor</span><span class="sxs-lookup"><span data-stu-id="913af-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="913af-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="913af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="913af-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="913af-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="913af-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="913af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="913af-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="913af-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="913af-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="913af-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="913af-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="913af-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="913af-126">DLL</span><span class="sxs-lookup"><span data-stu-id="913af-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="913af-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="913af-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





