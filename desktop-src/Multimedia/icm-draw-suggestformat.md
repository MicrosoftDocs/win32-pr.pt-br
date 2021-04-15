---
title: Mensagem de ICM_DRAW_SUGGESTFORMAT (VFW. h)
description: A \_ mensagem ICM Draw \_ SUGGESTFORMAT consulta um driver de renderização para sugerir um formato descompactado que pode ser desenhado.
ms.assetid: e3e97790-dbd1-4436-9830-5218ae1f949b
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_SUGGESTFORMAT
topic_type:
- apiref
api_name:
- ICM_DRAW_SUGGESTFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97c8782b16336427b3832f36b5a06987399df1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454808"
---
# <a name="icm_draw_suggestformat-message"></a><span data-ttu-id="cdeef-104">\_Mensagem de desenho SUGGESTFORMAT de ICM \_</span><span class="sxs-lookup"><span data-stu-id="cdeef-104">ICM\_DRAW\_SUGGESTFORMAT message</span></span>

<span data-ttu-id="cdeef-105">A mensagem **ICM \_ draw \_ SUGGESTFORMAT** consulta um driver de renderização para sugerir um formato descompactado que pode ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="cdeef-105">The **ICM\_DRAW\_SUGGESTFORMAT** message queries a rendering driver to suggest a decompressed format that it can draw.</span></span>


```C++
ICM_DRAW_SUGGESTFORMAT 
wParam = (DWORD_PTR) (LPVOID) &icdrwSuggest; 
lParam = sizeof(ICDRAWSUGGEST); 
```



## <a name="parameters"></a><span data-ttu-id="cdeef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdeef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdeef-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span><span class="sxs-lookup"><span data-stu-id="cdeef-107"><span id="icdrwSuggest"></span><span id="icdrwsuggest"></span><span id="ICDRWSUGGEST"></span>*icdrwSuggest*</span></span>
</dt> <dd>

<span data-ttu-id="cdeef-108">Ponteiro para uma estrutura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) .</span><span class="sxs-lookup"><span data-stu-id="cdeef-108">Pointer to an [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cdeef-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdeef-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="cdeef-110">Tamanho, em bytes, de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span><span class="sxs-lookup"><span data-stu-id="cdeef-110">Size, in bytes, of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdeef-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cdeef-111">Return Value</span></span>

<span data-ttu-id="cdeef-112">Retornará ICERR \_ OK se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="cdeef-112">Returns ICERR\_OK if successful.</span></span> <span data-ttu-id="cdeef-113">Se o membro **lpbiSuggest** da estrutura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) for **NULL**, essa mensagem retornará a quantidade de memória necessária para conter o formato sugerido.</span><span class="sxs-lookup"><span data-stu-id="cdeef-113">If the **lpbiSuggest** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure is **NULL**, this message returns the amount of memory required to contain the suggested format.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdeef-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdeef-114">Remarks</span></span>

<span data-ttu-id="cdeef-115">O driver deve examinar o formato especificado no membro **lpbiIn** da estrutura [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) e usar o membro **lpbiSuggest** para retornar um formato que ele possa desenhar.</span><span class="sxs-lookup"><span data-stu-id="cdeef-115">The driver should examine the format specified in the **lpbiIn** member of the [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) structure and use the **lpbiSuggest** member to return a format it can draw.</span></span> <span data-ttu-id="cdeef-116">O formato de saída deve preservar o máximo de dados possível do formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="cdeef-116">The output format should preserve as much data as possible from the input format.</span></span>

<span data-ttu-id="cdeef-117">Opcionalmente, o driver pode usar o identificador de compressor instalável passado no membro **hicDecompressor** de [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) para fazer seleções mais complexas.</span><span class="sxs-lookup"><span data-stu-id="cdeef-117">Optionally, the driver can use the installable compressor handle passed in the **hicDecompressor** member of [**ICDRAWSUGGEST**](/windows/desktop/api/Vfw/ns-vfw-icdrawsuggest) to make more complex selections.</span></span> <span data-ttu-id="cdeef-118">Por exemplo, se o formato de entrada for de dados JPEG de 24 bits, um renderizador poderá consultar o descompactador para descobrir se ele pode ser descompactado para um formato YUV (que pode ser desenhado com mais eficiência) antes de selecionar o formato a ser sugerido.</span><span class="sxs-lookup"><span data-stu-id="cdeef-118">For example, if the input format is 24-bit JPEG data, a renderer could query the decompressor to find out if it can decompress to a YUV format (which might be drawn more efficiently) before selecting the format to suggest.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdeef-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdeef-119">Requirements</span></span>



| <span data-ttu-id="cdeef-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdeef-120">Requirement</span></span> | <span data-ttu-id="cdeef-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cdeef-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cdeef-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdeef-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cdeef-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdeef-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cdeef-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdeef-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cdeef-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdeef-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cdeef-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cdeef-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdeef-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdeef-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdeef-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdeef-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdeef-129">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="cdeef-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="cdeef-130">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="cdeef-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





