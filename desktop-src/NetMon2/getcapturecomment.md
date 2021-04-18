---
description: Retorna um ponteiro para o comentário de uma captura.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Função GetCaptureComment (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766848"
---
# <a name="getcapturecomment-function"></a><span data-ttu-id="f2016-103">Função GetCaptureComment</span><span class="sxs-lookup"><span data-stu-id="f2016-103">GetCaptureComment function</span></span>

<span data-ttu-id="f2016-104">A função **GetCaptureComment** retorna um ponteiro para o comentário de uma captura.</span><span class="sxs-lookup"><span data-stu-id="f2016-104">The **GetCaptureComment** function returns a pointer to the comment of a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2016-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2016-105">Syntax</span></span>


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="f2016-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2016-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2016-107">*hCapture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2016-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2016-108">Um identificador para a captura.</span><span class="sxs-lookup"><span data-stu-id="f2016-108">A handle to the capture.</span></span> <span data-ttu-id="f2016-109">Para obter mais informações sobre como obter o identificador de captura, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="f2016-109">For more information about obtaining the capture handle, see the Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2016-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2016-110">Return value</span></span>

<span data-ttu-id="f2016-111">Se a função for bem-sucedida (ou seja, se a captura contiver um comentário), o valor de retorno será um ponteiro para a cadeia de caracteres de comentário.</span><span class="sxs-lookup"><span data-stu-id="f2016-111">If the function is successful (that is, if the capture contains a comment), the return value is a pointer to the comment string.</span></span>

<span data-ttu-id="f2016-112">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f2016-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2016-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2016-113">Remarks</span></span>

<span data-ttu-id="f2016-114">Não altere a cadeia de caracteres de comentário retornada, que é a cadeia de caracteres de comentário real que está na captura carregada.</span><span class="sxs-lookup"><span data-stu-id="f2016-114">Do not alter the returned comment string which is the actual comment string that is in the loaded capture.</span></span> <span data-ttu-id="f2016-115">As alterações podem corromper a captura.</span><span class="sxs-lookup"><span data-stu-id="f2016-115">Any changes can corrupt the capture.</span></span> <span data-ttu-id="f2016-116">Tentativas de modificar o resultado da cadeia de caracteres em uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="f2016-116">Attempts to modify the string result in an access violation.</span></span>

<span data-ttu-id="f2016-117">O identificador da captura pode ser obtido de várias maneiras, dependendo se a chamada é feita por um especialista ou analisador.</span><span class="sxs-lookup"><span data-stu-id="f2016-117">The handle of the capture can be obtained in several ways, depending if the call is made by an expert or parser.</span></span> <span data-ttu-id="f2016-118">Para especialistas, o identificador é especificado no membro **hCapture** da estrutura [EXPERTSTARTUPINFO](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f2016-118">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="f2016-119">Para analisadores, o identificador de captura pode ser obtido chamando a função [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="f2016-119">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="f2016-120">Para recuperar o comentário de uma captura de seu arquivo de captura, chame a função [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) .</span><span class="sxs-lookup"><span data-stu-id="f2016-120">To retrieve the comment of a capture from its capture file, call the [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) function.</span></span>

<span data-ttu-id="f2016-121">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetCaptureComment** .</span><span class="sxs-lookup"><span data-stu-id="f2016-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureComment** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2016-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2016-122">Requirements</span></span>



| <span data-ttu-id="f2016-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2016-123">Requirement</span></span> | <span data-ttu-id="f2016-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f2016-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f2016-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2016-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f2016-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2016-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f2016-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2016-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f2016-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f2016-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f2016-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f2016-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2016-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2016-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f2016-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2016-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2016-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2016-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2016-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f2016-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2016-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2016-134"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2016-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2016-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2016-136">EXPERTSTARTUPINFO</span><span class="sxs-lookup"><span data-stu-id="f2016-136">EXPERTSTARTUPINFO</span></span>](expertstartupinfo.md)
</dt> <dt>

[<span data-ttu-id="f2016-137">GetCaptureCommentFromFilename</span><span class="sxs-lookup"><span data-stu-id="f2016-137">GetCaptureCommentFromFilename</span></span>](getcapturecommentfromfilename.md)
</dt> <dt>

[<span data-ttu-id="f2016-138">GetFrameCaptureHandle</span><span class="sxs-lookup"><span data-stu-id="f2016-138">GetFrameCaptureHandle</span></span>](getframecapturehandle.md)
</dt> </dl>

 

 




