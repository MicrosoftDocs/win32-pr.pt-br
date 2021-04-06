---
description: A função GetCaptureTotalFrames retorna o número total de quadros na captura.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: Função GetCaptureTotalFrames (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826837"
---
# <a name="getcapturetotalframes-function"></a><span data-ttu-id="cae8a-103">Função GetCaptureTotalFrames</span><span class="sxs-lookup"><span data-stu-id="cae8a-103">GetCaptureTotalFrames function</span></span>

<span data-ttu-id="cae8a-104">A função **GetCaptureTotalFrames** retorna o número total de quadros na captura.</span><span class="sxs-lookup"><span data-stu-id="cae8a-104">The **GetCaptureTotalFrames** function returns the total number of frames in the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cae8a-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="cae8a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cae8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae8a-107">*hCapture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cae8a-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cae8a-108">Identificador para a captura.</span><span class="sxs-lookup"><span data-stu-id="cae8a-108">Handle to the capture.</span></span> <span data-ttu-id="cae8a-109">Para obter informações sobre como obter o identificador de captura, consulte a seção comentários deste tópico do **GetCaptureTotalFrames** .</span><span class="sxs-lookup"><span data-stu-id="cae8a-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTotalFrames** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae8a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cae8a-110">Return value</span></span>

<span data-ttu-id="cae8a-111">Se a função for bem-sucedida, o valor de retorno será o número total de quadros na captura.</span><span class="sxs-lookup"><span data-stu-id="cae8a-111">If the function is successful, the return value is the total number of frames in the capture.</span></span>

<span data-ttu-id="cae8a-112">Se a função não for bem-sucedida, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="cae8a-112">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae8a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cae8a-113">Remarks</span></span>

<span data-ttu-id="cae8a-114">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetCaptureTotalFrames** .</span><span class="sxs-lookup"><span data-stu-id="cae8a-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTotalFrames** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cae8a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cae8a-115">Requirements</span></span>



| <span data-ttu-id="cae8a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae8a-116">Requirement</span></span> | <span data-ttu-id="cae8a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cae8a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cae8a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cae8a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cae8a-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cae8a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cae8a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cae8a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cae8a-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cae8a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cae8a-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cae8a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cae8a-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cae8a-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cae8a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cae8a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="cae8a-125"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cae8a-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cae8a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cae8a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cae8a-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae8a-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




