---
description: A função GetFrame retorna um identificador para um determinado quadro dentro de uma captura.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Função GetFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089967"
---
# <a name="getframe-function"></a><span data-ttu-id="20ed4-103">Função GetFrame</span><span class="sxs-lookup"><span data-stu-id="20ed4-103">GetFrame function</span></span>

<span data-ttu-id="20ed4-104">A função **GetFrame** retorna um identificador para um determinado quadro dentro de uma captura.</span><span class="sxs-lookup"><span data-stu-id="20ed4-104">The **GetFrame** function returns a handle to a given frame within a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ed4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20ed4-105">Syntax</span></span>


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a><span data-ttu-id="20ed4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20ed4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20ed4-107">*hCapture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20ed4-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ed4-108">Identificador para uma captura.</span><span class="sxs-lookup"><span data-stu-id="20ed4-108">Handle to a capture.</span></span> <span data-ttu-id="20ed4-109">Para obter o identificador de captura, chame a função [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="20ed4-109">To obtain the capture handle, call the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="20ed4-110">*FrameNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20ed4-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20ed4-111">Número (baseado em zero) do quadro.</span><span class="sxs-lookup"><span data-stu-id="20ed4-111">Number (zero-based) of the frame.</span></span> <span data-ttu-id="20ed4-112">O número do primeiro quadro em uma captura é zero.</span><span class="sxs-lookup"><span data-stu-id="20ed4-112">The number of the first frame in a capture is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20ed4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20ed4-113">Return value</span></span>

<span data-ttu-id="20ed4-114">Se a função for bem-sucedida, o valor de retorno será um identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="20ed4-114">If the function is successful, the return value is a handle to the frame.</span></span>

<span data-ttu-id="20ed4-115">Se a função não for bem-sucedida (ou seja, se *hCapture* for inválido ou o número do quadro estiver fora do intervalo), o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="20ed4-115">If the function is unsuccessful (that is, if *hCapture* is invalid, or the frame number is out of range), the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="20ed4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="20ed4-116">Remarks</span></span>

<span data-ttu-id="20ed4-117">Use a função **GetFrame** para obter o identificador de quadro necessário ao localizar instâncias de uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="20ed4-117">Use the **GetFrame** function to obtain the frame handle needed when locating instances of a property.</span></span> <span data-ttu-id="20ed4-118">As funções usadas para localizar as instâncias de propriedade são [FindPropertyInstance](findpropertyinstance.md) que localiza a primeira instância e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) que localiza a próxima instância.</span><span class="sxs-lookup"><span data-stu-id="20ed4-118">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) which locates the first instance, and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) which locates the next instance.</span></span>

<span data-ttu-id="20ed4-119">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrame** .</span><span class="sxs-lookup"><span data-stu-id="20ed4-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ed4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20ed4-120">Requirements</span></span>



| <span data-ttu-id="20ed4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="20ed4-121">Requirement</span></span> | <span data-ttu-id="20ed4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="20ed4-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="20ed4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20ed4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="20ed4-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20ed4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="20ed4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20ed4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="20ed4-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20ed4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="20ed4-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="20ed4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="20ed4-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="20ed4-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="20ed4-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20ed4-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="20ed4-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20ed4-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="20ed4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="20ed4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20ed4-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20ed4-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ed4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="20ed4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ed4-134">FindPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="20ed4-134">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="20ed4-135">FindPropertyInstanceRestart</span><span class="sxs-lookup"><span data-stu-id="20ed4-135">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




