---
title: Mensagem de ICM_DECOMPRESS_QUERY (VFW. h)
description: A \_ mensagem de consulta de DEScompactação ICM \_ consulta um driver de descompactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode descompactar um formato de entrada específico para um formato de saída específico.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_QUERY
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758607"
---
# <a name="icm_decompress_query-message"></a><span data-ttu-id="a377e-104">\_Mensagem de consulta de DEScompactação ICM \_</span><span class="sxs-lookup"><span data-stu-id="a377e-104">ICM\_DECOMPRESS\_QUERY message</span></span>

<span data-ttu-id="a377e-105">A mensagem de **\_ \_ consulta de descompactação ICM** consulta um driver de descompactação de vídeo para determinar se ele dá suporte a um formato de entrada específico ou se pode descompactar um formato de entrada específico para um formato de saída específico.</span><span class="sxs-lookup"><span data-stu-id="a377e-105">The **ICM\_DECOMPRESS\_QUERY** message queries a video decompression driver to determine if it supports a specific input format or if it can decompress a specific input format to a specific output format.</span></span> <span data-ttu-id="a377e-106">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) .</span><span class="sxs-lookup"><span data-stu-id="a377e-106">You can send this message explicitly or by using the [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) macro.</span></span>


```C++
ICM_DECOMPRESS_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="a377e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a377e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a377e-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="a377e-108"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="a377e-109">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="a377e-109">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="a377e-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="a377e-110"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="a377e-111">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="a377e-111">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span> <span data-ttu-id="a377e-112">Você pode especificar zero para esse parâmetro para indicar que qualquer formato de saída é aceitável.</span><span class="sxs-lookup"><span data-stu-id="a377e-112">You can specify zero for this parameter to indicate any output format is acceptable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a377e-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a377e-113">Return Value</span></span>

<span data-ttu-id="a377e-114">Retornará ICERR \_ OK se a descompactação especificada for suportada ou ICERR \_ BADFORMAT do contrário.</span><span class="sxs-lookup"><span data-stu-id="a377e-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a377e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a377e-115">Requirements</span></span>



| <span data-ttu-id="a377e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a377e-116">Requirement</span></span> | <span data-ttu-id="a377e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a377e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a377e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a377e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a377e-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a377e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a377e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a377e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a377e-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a377e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a377e-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a377e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a377e-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a377e-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a377e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a377e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a377e-125">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="a377e-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a377e-126">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="a377e-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

