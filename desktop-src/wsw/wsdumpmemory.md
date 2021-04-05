---
title: Função WsDumpMemory (WebServicesDebug. h)
description: Essa função despeja todas as alocações de memória para o console.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Serviços Web da função WsDumpMemory para Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918923"
---
# <a name="wsdumpmemory-function"></a><span data-ttu-id="ac94b-104">Função WsDumpMemory</span><span class="sxs-lookup"><span data-stu-id="ac94b-104">WsDumpMemory function</span></span>

<span data-ttu-id="ac94b-105">Essa função despeja todas as alocações de memória para o console.</span><span class="sxs-lookup"><span data-stu-id="ac94b-105">This function dumps all memory allocations to the console.</span></span>

> [!Note]  
> <span data-ttu-id="ac94b-106">Essa função é somente para depuração.</span><span class="sxs-lookup"><span data-stu-id="ac94b-106">This function is for DEBUG ONLY.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ac94b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac94b-107">Syntax</span></span>


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="ac94b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac94b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac94b-109">*erro* \[ do em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ac94b-109">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac94b-110">Um ponteiro para um objeto de [ \_ erro WS](ws-error.md) em que informações adicionais sobre o erro devem ser armazenadas se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="ac94b-110">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac94b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac94b-111">Return value</span></span>

<span data-ttu-id="ac94b-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ac94b-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac94b-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac94b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac94b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac94b-114">Requirements</span></span>



| <span data-ttu-id="ac94b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac94b-115">Requirement</span></span> | <span data-ttu-id="ac94b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ac94b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac94b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac94b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ac94b-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ac94b-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                             |
| <span data-ttu-id="ac94b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac94b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ac94b-120">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ac94b-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="ac94b-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac94b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac94b-122"><dt>WebServicesDebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac94b-122"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





