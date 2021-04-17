---
description: A função ModifyFrame altera um quadro existente com novos dados.
ms.assetid: ebd248e4-b248-4f4a-8b94-a6d1c331d12a
title: Função ModifyFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ModifyFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: af3ef6c2c5ccae2b6410ac8fc81c815f790b17a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749239"
---
# <a name="modifyframe-function"></a><span data-ttu-id="f8ef1-103">Função ModifyFrame</span><span class="sxs-lookup"><span data-stu-id="f8ef1-103">ModifyFrame function</span></span>

<span data-ttu-id="f8ef1-104">A função **ModifyFrame** altera um quadro existente com novos dados.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-104">The **ModifyFrame** function alters an existing frame with new data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ef1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8ef1-105">Syntax</span></span>


```C++
HFRAME WINAPI ModifyFrame(
  _In_  HCAPTURE hCapture,
  _In_  DWORD    FrameNumber,
  _In_  LPBYTE   FrameData,
  _In_  DWORD    FrameLength,
  _Out_ __int64  TimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="f8ef1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8ef1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ef1-107">*hCapture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8ef1-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ef1-108">Identificador para a captura.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-108">Handle to the capture.</span></span> <span data-ttu-id="f8ef1-109">Para obter informações sobre como obter o identificador de captura, consulte a seção comentários deste tópico do **ModifyFrame** .</span><span class="sxs-lookup"><span data-stu-id="f8ef1-109">For information about obtaining the capture handle, see the Remarks section of this **ModifyFrame** topic.</span></span>

</dd> <dt>

<span data-ttu-id="f8ef1-110">*FrameNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8ef1-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ef1-111">Número de índice do quadro.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-111">Frame index number.</span></span>

</dd> <dt>

<span data-ttu-id="f8ef1-112">*FrameData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8ef1-112">*FrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ef1-113">Ponteiro para uma matriz de bytes que contém os novos dados de quadro.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-113">Pointer to an array of bytes that contain the new frame data.</span></span>

</dd> <dt>

<span data-ttu-id="f8ef1-114">*FrameLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8ef1-114">*FrameLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ef1-115">Comprimento dos novos dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-115">Length of the new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f8ef1-116">*Timestamp* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f8ef1-116">*TimeStamp* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ef1-117">Carimbo de data/hora que indica quando o quadro foi modificado.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-117">Time stamp indicating when the frame was modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ef1-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8ef1-118">Return value</span></span>

<span data-ttu-id="f8ef1-119">Se a função for bem-sucedida, o valor de retorno será um identificador para um novo quadro.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-119">If the function is successful, the return value is a handle to a new frame.</span></span>

<span data-ttu-id="f8ef1-120">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-120">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ef1-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8ef1-121">Remarks</span></span>

<span data-ttu-id="f8ef1-122">Se a chamada for bem-sucedida, a função **ModifyFrame** destruirá o quadro original.</span><span class="sxs-lookup"><span data-stu-id="f8ef1-122">If the call is successful, the **ModifyFrame** function destroys the original frame.</span></span>

<span data-ttu-id="f8ef1-123">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **ModifyFrame** .</span><span class="sxs-lookup"><span data-stu-id="f8ef1-123">[*Experts*](e.md) and [*parsers*](p.md) can call the **ModifyFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ef1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8ef1-124">Requirements</span></span>



| <span data-ttu-id="f8ef1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8ef1-125">Requirement</span></span> | <span data-ttu-id="f8ef1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f8ef1-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ef1-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8ef1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ef1-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8ef1-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f8ef1-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8ef1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ef1-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f8ef1-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f8ef1-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f8ef1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8ef1-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ef1-132"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f8ef1-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8ef1-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8ef1-134"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8ef1-134"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8ef1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f8ef1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8ef1-136"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8ef1-136"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




