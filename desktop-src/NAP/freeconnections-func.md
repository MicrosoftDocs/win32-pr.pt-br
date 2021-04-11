---
title: Função FreeConnections (NapUtil. h)
description: Libera uma estrutura de dados de conexões.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- Função FreeConnections NAP
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f840d02572af3e6382a06a1873573fc7a30420e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294763"
---
# <a name="freeconnections-function"></a><span data-ttu-id="d136c-104">Função FreeConnections</span><span class="sxs-lookup"><span data-stu-id="d136c-104">FreeConnections function</span></span>

> [!Note]  
> <span data-ttu-id="d136c-105">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="d136c-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d136c-106">A função **FreeConnections** libera uma estrutura de dados de [**conexões**](connections-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="d136c-106">The **FreeConnections** function frees a [**Connections**](connections-struct.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d136c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d136c-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a><span data-ttu-id="d136c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d136c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d136c-109">*conexões* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d136c-109">*connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d136c-110">Um ponteiro para a estrutura de [**conexões**](connections-struct.md) para gratuito.</span><span class="sxs-lookup"><span data-stu-id="d136c-110">A pointer to the [**Connections**](connections-struct.md) structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d136c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d136c-111">Remarks</span></span>

<span data-ttu-id="d136c-112">Todas as interfaces COM com suporte do sistema NAP usam regras de gerenciamento de memória COM padrão e os alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="d136c-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="d136c-113">**Em** parâmetros são alocados e liberados pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="d136c-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="d136c-114">Os parâmetros de **saída** são alocados pelo receptor e liberados pelo chamador usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="d136c-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="d136c-115">Os parâmetros **in/out** são alocados pelo chamador, liberados e realocados pelo receptor e, por fim, liberados pelo chamador, usando **CoTaskMem**.</span><span class="sxs-lookup"><span data-stu-id="d136c-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="d136c-116">Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="d136c-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d136c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d136c-117">Requirements</span></span>



| <span data-ttu-id="d136c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d136c-118">Requirement</span></span> | <span data-ttu-id="d136c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d136c-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d136c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d136c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d136c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d136c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d136c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d136c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d136c-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d136c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d136c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d136c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d136c-125"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="d136c-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="d136c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d136c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d136c-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d136c-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d136c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d136c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d136c-129">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="d136c-129">**AllocConnections**</span></span>](allocconnections-func.md)
</dt> </dl>

 

 





