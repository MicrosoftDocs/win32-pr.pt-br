---
description: A função GetCaptureCommentFromFilename extrai o comentário de captura de um arquivo de captura.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Função GetCaptureCommentFromFilename (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810297"
---
# <a name="getcapturecommentfromfilename-function"></a><span data-ttu-id="68dd8-103">Função GetCaptureCommentFromFilename</span><span class="sxs-lookup"><span data-stu-id="68dd8-103">GetCaptureCommentFromFilename function</span></span>

<span data-ttu-id="68dd8-104">A função **GetCaptureCommentFromFilename** extrai o comentário de captura de um [*arquivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="68dd8-104">The **GetCaptureCommentFromFilename** function extracts the capture comment from a [*capture file*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68dd8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68dd8-105">Syntax</span></span>


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="68dd8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68dd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68dd8-107">*lpFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68dd8-107">*lpFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68dd8-108">Ponteiro para o nome do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="68dd8-108">Pointer to the name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="68dd8-109">*lpComment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68dd8-109">*lpComment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68dd8-110">Ponteiro para uma cadeia de caracteres alocada previamente para o comentário.</span><span class="sxs-lookup"><span data-stu-id="68dd8-110">Pointer to a pre-allocated string for the comment.</span></span>

</dd> <dt>

<span data-ttu-id="68dd8-111">*BufferSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68dd8-111">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68dd8-112">Tamanho da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="68dd8-112">Size of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68dd8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68dd8-113">Return value</span></span>

<span data-ttu-id="68dd8-114">Se a função for bem-sucedida (ou seja, se o comentário for encontrado e copiado, ou não houver nenhum comentário no arquivo de captura), o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="68dd8-114">If the function is successful (that is, if the comment is found and copied, or there is no comment in the capture file), the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="68dd8-115">Se a função não for bem-sucedida, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="68dd8-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="68dd8-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="68dd8-116">Return code</span></span>                                                                                                 | <span data-ttu-id="68dd8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="68dd8-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68dd8-118"><dt>**\_erro de \_ leitura do arquivo NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68dd8-118"><dt>**NMERR\_FILE\_READ\_ERROR**</dt></span></span> </dl>     | <span data-ttu-id="68dd8-119">Não é possível ler o comentário de captura.</span><span class="sxs-lookup"><span data-stu-id="68dd8-119">The capture comment cannot be read.</span></span><br/>                               |
| <dl> <span data-ttu-id="68dd8-120"><dt>**NMERR \_ \_ formato de arquivo inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="68dd8-120"><dt>**NMERR\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="68dd8-121">O quadro de comentário não é um formato de arquivo válido.</span><span class="sxs-lookup"><span data-stu-id="68dd8-121">The Comment frame is not a valid file format.</span></span><br/>                     |
| <dl> <span data-ttu-id="68dd8-122"><dt>**\_arquivo NMERR \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="68dd8-122"><dt>**NMERR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>      | <span data-ttu-id="68dd8-123">O arquivo especificado pelo parâmetro *lpFileName* não pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="68dd8-123">The file specified by the *lpFilename* parameter cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="68dd8-124"><dt>**NMERR \_ \_ parâmetro inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="68dd8-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="68dd8-125">Um dos parâmetros foi especificado incorretamente.</span><span class="sxs-lookup"><span data-stu-id="68dd8-125">One of the parameters is specified incorrectly.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="68dd8-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="68dd8-126">Remarks</span></span>

<span data-ttu-id="68dd8-127">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetCaptureCommentFromFilename** .</span><span class="sxs-lookup"><span data-stu-id="68dd8-127">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureCommentFromFilename** function.</span></span>

<span data-ttu-id="68dd8-128">Para recuperar o comentário de uma captura em tempo real, chame a função [GetCaptureComment](getcapturecomment.md) .</span><span class="sxs-lookup"><span data-stu-id="68dd8-128">To retrieve the comment of a real-time capture, call the [GetCaptureComment](getcapturecomment.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="68dd8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68dd8-129">Requirements</span></span>



| <span data-ttu-id="68dd8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="68dd8-130">Requirement</span></span> | <span data-ttu-id="68dd8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="68dd8-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="68dd8-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68dd8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="68dd8-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="68dd8-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="68dd8-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68dd8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="68dd8-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="68dd8-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="68dd8-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="68dd8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="68dd8-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="68dd8-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="68dd8-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68dd8-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="68dd8-139"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68dd8-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="68dd8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="68dd8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68dd8-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68dd8-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68dd8-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="68dd8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68dd8-143">GetCaptureComment</span><span class="sxs-lookup"><span data-stu-id="68dd8-143">GetCaptureComment</span></span>](getcapturecomment.md)
</dt> </dl>

 

 




