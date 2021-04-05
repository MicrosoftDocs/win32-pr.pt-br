---
title: IMAGELISTSTATEFLAGS (commctrl. h)
description: Os sinalizadores a seguir são passados para o método de desenho IImageList no membro fState de IMAGELISTDRAWPARAMS.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009203"
---
# <a name="imageliststateflags"></a><span data-ttu-id="6bc15-103">IMAGELISTSTATEFLAGS</span><span class="sxs-lookup"><span data-stu-id="6bc15-103">IMAGELISTSTATEFLAGS</span></span>

<span data-ttu-id="6bc15-104">Os sinalizadores a seguir são passados para o método [**bruto IImageList::D**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) no membro **fState** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span><span class="sxs-lookup"><span data-stu-id="6bc15-104">The following flags are passed to the [**IImageList::Draw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) method in the **fState** member of [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span></span>



| <span data-ttu-id="6bc15-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="6bc15-105">Constant/value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="6bc15-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6bc15-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <span data-ttu-id="6bc15-107"><dt>**ILS \_ NORMAL**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="6bc15-107"><dt>**ILS\_NORMAL**</dt> <dt>0x00000000</dt></span></span> </dl>       | <span data-ttu-id="6bc15-108">O estado da imagem não é modificado.</span><span class="sxs-lookup"><span data-stu-id="6bc15-108">The image state is not modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <span data-ttu-id="6bc15-109"><dt>**ILS \_ BRILHO**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6bc15-109"><dt>**ILS\_GLOW**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="6bc15-110">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="6bc15-110">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <span data-ttu-id="6bc15-111"><dt>**ILS \_ SOMBRA**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="6bc15-111"><dt>**ILS\_SHADOW**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="6bc15-112">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="6bc15-112">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <span data-ttu-id="6bc15-113"><dt>**ILS \_ Saturação**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="6bc15-113"><dt>**ILS\_SATURATE**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="6bc15-114">Reduz a saturação de cor do ícone para escala de cinza.</span><span class="sxs-lookup"><span data-stu-id="6bc15-114">Reduces the color saturation of the icon to grayscale.</span></span> <span data-ttu-id="6bc15-115">Isso afeta apenas as imagens 32 bpp.</span><span class="sxs-lookup"><span data-stu-id="6bc15-115">This only affects 32bpp images.</span></span> <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <span data-ttu-id="6bc15-116"><dt>**ILS \_**</dt> <dt>0x00000008</dt> alfa</span><span class="sxs-lookup"><span data-stu-id="6bc15-116"><dt>**ILS\_ALPHA**</dt> <dt>0x00000008</dt></span></span> </dl>          | <span data-ttu-id="6bc15-117">Alfa mistura o ícone.</span><span class="sxs-lookup"><span data-stu-id="6bc15-117">Alpha blends the icon.</span></span> <span data-ttu-id="6bc15-118">A mesclagem alfa controla o nível de transparência de um ícone, de acordo com o valor de seu canal alfa.</span><span class="sxs-lookup"><span data-stu-id="6bc15-118">Alpha blending controls the transparency level of an icon, according to the value of its alpha channel.</span></span> <span data-ttu-id="6bc15-119">O valor do canal alfa é indicado pelo membro de **quadro** no método [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) .</span><span class="sxs-lookup"><span data-stu-id="6bc15-119">The value of the alpha channel is indicated by the **frame** member in the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) method.</span></span> <span data-ttu-id="6bc15-120">O canal alfa pode ser de 0 a 255, sendo que 0 é completamente transparente e 255 sendo completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="6bc15-120">The alpha channel can be from 0 to 255, with 0 being completely transparent, and 255 being completely opaque.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6bc15-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bc15-121">Requirements</span></span>



| <span data-ttu-id="6bc15-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bc15-122">Requirement</span></span> | <span data-ttu-id="6bc15-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6bc15-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc15-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bc15-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6bc15-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6bc15-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6bc15-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6bc15-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6bc15-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6bc15-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6bc15-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6bc15-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bc15-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bc15-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

