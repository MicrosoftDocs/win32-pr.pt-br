---
description: Este tópico lista os métodos SaveAdd da classe Image. Para obter uma lista completa de métodos para a classe Image, consulte métodos de imagem.
ms.assetid: e597f6e6-6e07-4afb-8905-26e4af961685
title: Métodos Image. SaveAdd (Gdiplusheaders. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a2b65c6fe56507538f092edc7128497de5cb2f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967841"
---
# <a name="imagesaveadd-methods"></a><span data-ttu-id="00d05-104">Métodos Image. SaveAdd</span><span class="sxs-lookup"><span data-stu-id="00d05-104">Image.SaveAdd methods</span></span>

<span data-ttu-id="00d05-105">Este tópico lista os métodos SaveAdd da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) .</span><span class="sxs-lookup"><span data-stu-id="00d05-105">This topic lists the SaveAdd methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class.</span></span> <span data-ttu-id="00d05-106">Para obter uma lista completa de métodos para a classe **Image** , consulte [métodos de imagem](-gdiplus-class-image-methods.md).</span><span class="sxs-lookup"><span data-stu-id="00d05-106">For a complete list of methods for the **Image** class, see [Image Methods](-gdiplus-class-image-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="00d05-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="00d05-107">Overload list</span></span>



| <span data-ttu-id="00d05-108">Método</span><span class="sxs-lookup"><span data-stu-id="00d05-108">Method</span></span>                                                                                               | <span data-ttu-id="00d05-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="00d05-109">Description</span></span>                                                                                                                                                                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d05-110">[**SaveAdd (EncoderParameters \* )**](/previous-versions//ms535408(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="00d05-110">[**SaveAdd(EncoderParameters\*)**](/previous-versions//ms535408(v=vs.85))</span></span>                  | <span data-ttu-id="00d05-111">O método [**Image:: SaveAdd**](/previous-versions//ms535408(v=vs.85)) adiciona um quadro a um arquivo ou fluxo especificado em uma chamada anterior para o método **Save** .</span><span class="sxs-lookup"><span data-stu-id="00d05-111">The [**Image::SaveAdd**](/previous-versions//ms535408(v=vs.85)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span> <span data-ttu-id="00d05-112">Use esse método para salvar quadros selecionados de uma imagem de vários quadros em outra imagem de vários quadros.</span><span class="sxs-lookup"><span data-stu-id="00d05-112">Use this method to save selected frames from a multiple-frame image to another multiple-frame image.</span></span><br/> |
| <span data-ttu-id="00d05-113">[**SaveAdd (imagem \* , codificador \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span><span class="sxs-lookup"><span data-stu-id="00d05-113">[**SaveAdd(Image\*,EncoderParameters\*)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters))</span></span> | <span data-ttu-id="00d05-114">O método [**Image:: SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) adiciona um quadro a um arquivo ou fluxo especificado em uma chamada anterior para o método **Save** .</span><span class="sxs-lookup"><span data-stu-id="00d05-114">The [**Image::SaveAdd**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) method adds a frame to a file or stream specified in a previous call to the **Save** method.</span></span><br/>                                                                                             |



## <a name="requirements"></a><span data-ttu-id="00d05-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00d05-115">Requirements</span></span>



| <span data-ttu-id="00d05-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d05-116">Requirement</span></span> | <span data-ttu-id="00d05-117">Valor</span><span class="sxs-lookup"><span data-stu-id="00d05-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d05-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00d05-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00d05-119">Somente aplicativos de desktop do Windows XP, Windows 2000 Professional \[\]</span><span class="sxs-lookup"><span data-stu-id="00d05-119">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="00d05-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00d05-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00d05-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="00d05-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="00d05-122">Produto</span><span class="sxs-lookup"><span data-stu-id="00d05-122">Product</span></span><br/>                  | <span data-ttu-id="00d05-123">GDI+ 1,0</span><span class="sxs-lookup"><span data-stu-id="00d05-123">GDI+ 1.0</span></span><br/>                                                                                             |
| <span data-ttu-id="00d05-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00d05-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="00d05-125"><dt>Gdiplusheaders. h (incluir Gdiplus. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00d05-125"><dt>Gdiplusheaders.h (include Gdiplus.h)</dt></span></span> </dl> |
| <span data-ttu-id="00d05-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00d05-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="00d05-127"><dt>Gdiplus. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00d05-127"><dt>Gdiplus.lib</dt></span></span> </dl>                          |



 

 
