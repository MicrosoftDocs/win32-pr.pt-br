---
title: Mensagem de ICM_COMPRESS (VFW. h)
description: A \_ mensagem de compactação ICM notifica um driver de compactação de vídeo para compactar um quadro de dados em um buffer definido pelo aplicativo.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8021a4c18ab47c9b5b848dd1cb097358f2714bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748130"
---
# <a name="icm_compress-message"></a><span data-ttu-id="febf1-104">\_Mensagem de compactação ICM</span><span class="sxs-lookup"><span data-stu-id="febf1-104">ICM\_COMPRESS message</span></span>

<span data-ttu-id="febf1-105">A mensagem de **\_ compactação ICM** notifica um driver de compactação de vídeo para compactar um quadro de dados em um buffer definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="febf1-105">The **ICM\_COMPRESS** message notifies a video compression driver to compress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="febf1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="febf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="febf1-107"><span id="icc"></span><span id="ICC"></span>*ICC*</span><span class="sxs-lookup"><span data-stu-id="febf1-107"><span id="icc"></span><span id="ICC"></span>*icc*</span></span>
</dt> <dd>

<span data-ttu-id="febf1-108">Ponteiro para uma estrutura [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) .</span><span class="sxs-lookup"><span data-stu-id="febf1-108">Pointer to an [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) structure.</span></span> <span data-ttu-id="febf1-109">Os seguintes membros dessa estrutura especificam os parâmetros de compactação: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** e **dwQuality**.</span><span class="sxs-lookup"><span data-stu-id="febf1-109">The following members of this structure specify the compression parameters: **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize**, and **dwQuality**.</span></span> <span data-ttu-id="febf1-110">O driver também deve usar o membro **biSizeImage** da estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) associada ao **lpbiOutput** de **ICCOMPRESS** para retornar o tamanho do quadro compactado.</span><span class="sxs-lookup"><span data-stu-id="febf1-110">The driver should also use the **biSizeImage** member of the [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure associated with **lpbiOutput** of **ICCOMPRESS** to return the size of the compressed frame.</span></span>

</dd> <dt>

<span data-ttu-id="febf1-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="febf1-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="febf1-112">Tamanho, em bytes, de [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span><span class="sxs-lookup"><span data-stu-id="febf1-112">Size, in bytes, of [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="febf1-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="febf1-113">Return Value</span></span>

<span data-ttu-id="febf1-114">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="febf1-114">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="febf1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="febf1-115">Requirements</span></span>



| <span data-ttu-id="febf1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="febf1-116">Requirement</span></span> | <span data-ttu-id="febf1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="febf1-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="febf1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="febf1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="febf1-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="febf1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="febf1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="febf1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="febf1-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="febf1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="febf1-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="febf1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="febf1-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="febf1-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="febf1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="febf1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="febf1-125">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="febf1-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="febf1-126">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="febf1-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

