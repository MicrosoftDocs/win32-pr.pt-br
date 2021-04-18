---
title: Mensagem de ICM_COMPRESS_QUERY (VFW. h)
description: A \_ mensagem de consulta de compactação ICM \_ consulta um driver de compactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode compactar um formato de entrada específico para um formato de saída específico.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_QUERY
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a00482cc39f21ef6ddfb241f0534924c503200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105768710"
---
# <a name="icm_compress_query-message"></a><span data-ttu-id="e1456-104">\_Mensagem de consulta de compactação ICM \_</span><span class="sxs-lookup"><span data-stu-id="e1456-104">ICM\_COMPRESS\_QUERY message</span></span>

<span data-ttu-id="e1456-105">A mensagem de **\_ \_ consulta de compactação ICM** consulta um driver de compactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode compactar um formato de entrada específico para um formato de saída específico.</span><span class="sxs-lookup"><span data-stu-id="e1456-105">The **ICM\_COMPRESS\_QUERY** message queries a video compression driver to determine if it supports a specific input format or if it can compress a specific input format to a specific output format.</span></span> <span data-ttu-id="e1456-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) .</span><span class="sxs-lookup"><span data-stu-id="e1456-106">You can send this message explicitly or by using the [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) macro.</span></span>


```C++
ICM_COMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="e1456-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1456-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1456-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="e1456-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="e1456-109">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1456-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="e1456-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="e1456-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="e1456-111">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="e1456-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="e1456-112">Você pode especificar zero para esse parâmetro para indicar que qualquer formato de saída é aceitável.</span><span class="sxs-lookup"><span data-stu-id="e1456-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1456-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e1456-113">Return Value</span></span>

<span data-ttu-id="e1456-114">Retornará ICERR \_ OK se a compactação especificada for suportada ou ICERR \_ BADFORMAT caso contrário.</span><span class="sxs-lookup"><span data-stu-id="e1456-114">Returns ICERR\_OK if the specified compression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1456-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1456-115">Remarks</span></span>

<span data-ttu-id="e1456-116">Quando um driver recebe essa mensagem, ele deve examinar a estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) associada ao *lpbiInput* para determinar se ele pode compactar o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1456-116">When a driver receives this message, it should examine the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure associated with *lpbiInput* to determine if it can compress the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1456-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1456-117">Requirements</span></span>



| <span data-ttu-id="e1456-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1456-118">Requirement</span></span> | <span data-ttu-id="e1456-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e1456-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1456-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1456-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e1456-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1456-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e1456-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1456-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e1456-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e1456-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1456-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e1456-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1456-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1456-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1456-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1456-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1456-127">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1456-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="e1456-128">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="e1456-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

