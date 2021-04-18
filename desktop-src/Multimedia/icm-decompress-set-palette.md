---
title: Mensagem de ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: A \_ mensagem de paleta do conjunto de DEScompactação ICM \_ \_ especifica uma paleta para um driver de descompactação de vídeo a ser usado se estiver descompactando para um formato que usa uma paleta. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_SET_PALETTE
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759629"
---
# <a name="icm_decompress_set_palette-message"></a><span data-ttu-id="0689e-105">Mensagem de paleta do conjunto de \_ DEScompactação ICM \_ \_</span><span class="sxs-lookup"><span data-stu-id="0689e-105">ICM\_DECOMPRESS\_SET\_PALETTE message</span></span>

<span data-ttu-id="0689e-106">A mensagem de **\_ paleta do \_ conjunto \_ de descompactação ICM** especifica uma paleta para um driver de descompactação de vídeo a ser usado se estiver descompactando para um formato que usa uma paleta.</span><span class="sxs-lookup"><span data-stu-id="0689e-106">The **ICM\_DECOMPRESS\_SET\_PALETTE** message specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette.</span></span> <span data-ttu-id="0689e-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .</span><span class="sxs-lookup"><span data-stu-id="0689e-107">You can send this message explicitly or by using the [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="0689e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0689e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0689e-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span><span class="sxs-lookup"><span data-stu-id="0689e-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span></span>
</dt> <dd>

<span data-ttu-id="0689e-110">Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) cuja tabela de cores contém as cores que devem ser usadas, se possível.</span><span class="sxs-lookup"><span data-stu-id="0689e-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure whose color table contains the colors that should be used if possible.</span></span> <span data-ttu-id="0689e-111">Você pode especificar zero para usar o conjunto padrão de cores de saída.</span><span class="sxs-lookup"><span data-stu-id="0689e-111">You can specify zero to use the default set of output colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0689e-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0689e-112">Return Value</span></span>

<span data-ttu-id="0689e-113">Retornará ICERR \_ OK se o driver de descompactação puder descompactar precisamente as imagens para a paleta sugerida usando o conjunto de cores conforme elas forem organizadas na paleta.</span><span class="sxs-lookup"><span data-stu-id="0689e-113">Returns ICERR\_OK if the decompression driver can precisely decompress images to the suggested palette using the set of colors as they are arranged in the palette.</span></span> <span data-ttu-id="0689e-114">Retorna ICERR \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="0689e-114">Returns ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0689e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0689e-115">Remarks</span></span>

<span data-ttu-id="0689e-116">Esta mensagem não deve afetar a descompactação já em andamento; em vez disso, as cores passadas usando essa mensagem devem ser retornadas em resposta ao futuro [**ICM \_ descompactar \_ Get \_ Format**](icm-decompress-get-format.md) e [**ICM \_ descompactar \_ \_**](icm-decompress-get-palette.md) as mensagens da paleta.</span><span class="sxs-lookup"><span data-stu-id="0689e-116">This message should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future [**ICM\_DECOMPRESS\_GET\_FORMAT**](icm-decompress-get-format.md) and [**ICM\_DECOMPRESS\_GET\_PALETTE**](icm-decompress-get-palette.md) messages.</span></span> <span data-ttu-id="0689e-117">As cores são enviadas de volta para o driver de descompactação em uma futura mensagem de [**\_ \_ início de descompactação ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="0689e-117">Colors are sent back to the decompression driver in a future [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="0689e-118">Essa mensagem é usada principalmente quando um driver Descompacte imagens na tela e outro aplicativo que usa uma paleta está em primeiro plano, forçando o driver de descompactação a se adaptar a um conjunto de cores estrangeiro.</span><span class="sxs-lookup"><span data-stu-id="0689e-118">This message is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.</span></span>

## <a name="requirements"></a><span data-ttu-id="0689e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0689e-119">Requirements</span></span>



| <span data-ttu-id="0689e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0689e-120">Requirement</span></span> | <span data-ttu-id="0689e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0689e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0689e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0689e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0689e-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0689e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0689e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0689e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0689e-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0689e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0689e-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0689e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0689e-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0689e-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0689e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="0689e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0689e-129">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="0689e-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0689e-130">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="0689e-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

