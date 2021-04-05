---
description: A função GetFrameCaptureHandle retorna um identificador para a captura com base em um determinado quadro.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Função GetFrameCaptureHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826835"
---
# <a name="getframecapturehandle-function"></a><span data-ttu-id="af41d-103">Função GetFrameCaptureHandle</span><span class="sxs-lookup"><span data-stu-id="af41d-103">GetFrameCaptureHandle function</span></span>

<span data-ttu-id="af41d-104">A função **GetFrameCaptureHandle** retorna um identificador para a captura com base em um determinado quadro.</span><span class="sxs-lookup"><span data-stu-id="af41d-104">The **GetFrameCaptureHandle** function returns a handle to the capture based on a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="af41d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af41d-105">Syntax</span></span>


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="af41d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af41d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af41d-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af41d-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af41d-108">Identificador para um quadro.</span><span class="sxs-lookup"><span data-stu-id="af41d-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af41d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af41d-109">Return value</span></span>

<span data-ttu-id="af41d-110">Se a função for bem-sucedida, o valor de retorno será um identificador para a captura.</span><span class="sxs-lookup"><span data-stu-id="af41d-110">If the function is successful, the return value is a handle to the capture.</span></span>

<span data-ttu-id="af41d-111">Se a função não for bem-sucedida, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="af41d-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="af41d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="af41d-112">Remarks</span></span>

<span data-ttu-id="af41d-113">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameCaptureHandle** .</span><span class="sxs-lookup"><span data-stu-id="af41d-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameCaptureHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="af41d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af41d-114">Requirements</span></span>



| <span data-ttu-id="af41d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="af41d-115">Requirement</span></span> | <span data-ttu-id="af41d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="af41d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="af41d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af41d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af41d-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="af41d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="af41d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af41d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af41d-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="af41d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="af41d-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="af41d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="af41d-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="af41d-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="af41d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af41d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="af41d-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af41d-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="af41d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="af41d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af41d-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af41d-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




