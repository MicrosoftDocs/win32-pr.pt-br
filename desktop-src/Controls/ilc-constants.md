---
title: Sinalizadores de criação da lista de imagens (shlobj. h)
description: O conjunto de sinalizadores de bits que especifica o tipo de lista de imagens a ser criado. Esse parâmetro pode ser uma combinação dos valores a seguir, mas pode incluir apenas um dos \_ valores de cor ILC. Usado por ImageList \_ Create e IImageList2 Initialize.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455013"
---
# <a name="image-list-creation-flags"></a><span data-ttu-id="3031c-105">Sinalizadores de criação da lista de imagens</span><span class="sxs-lookup"><span data-stu-id="3031c-105">Image List Creation Flags</span></span>

<span data-ttu-id="3031c-106">O conjunto de sinalizadores de bits que especifica o tipo de lista de imagens a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3031c-106">The set of bit flags that specifies the type of image list to create.</span></span> <span data-ttu-id="3031c-107">Esse parâmetro pode ser uma combinação dos valores a seguir, mas pode incluir apenas um dos \_ valores de cor ILC.</span><span class="sxs-lookup"><span data-stu-id="3031c-107">This parameter can be a combination of the following values, but it can include only one of the ILC\_COLOR values.</span></span> <span data-ttu-id="3031c-108">Usado por [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) e [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span><span class="sxs-lookup"><span data-stu-id="3031c-108">Used by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) and [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span></span>



| <span data-ttu-id="3031c-109">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="3031c-109">Constant/value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="3031c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3031c-110">Description</span></span>                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <span data-ttu-id="3031c-111"><dt>**ILC \_ MÁSCARA**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-111"><dt>**ILC\_MASK**</dt> <dt>0x00000001</dt></span></span> </dl>                                     | <span data-ttu-id="3031c-112">Use uma máscara.</span><span class="sxs-lookup"><span data-stu-id="3031c-112">Use a mask.</span></span> <span data-ttu-id="3031c-113">A lista de imagens contém dois bitmaps, um dos quais é um bitmap monocromático usado como uma máscara.</span><span class="sxs-lookup"><span data-stu-id="3031c-113">The image list contains two bitmaps, one of which is a monochrome bitmap used as a mask.</span></span> <span data-ttu-id="3031c-114">Se esse valor não for incluído, a lista de imagens conterá apenas um bitmap.</span><span class="sxs-lookup"><span data-stu-id="3031c-114">If this value is not included, the image list contains only one bitmap.</span></span><br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <span data-ttu-id="3031c-115"><dt>**ILC \_ COR**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-115"><dt>**ILC\_COLOR**</dt> <dt>0x00000000</dt></span></span> </dl>                                  | <span data-ttu-id="3031c-116">Use o comportamento padrão se nenhum dos outros sinalizadores de \_ COLORx de ILC for especificado.</span><span class="sxs-lookup"><span data-stu-id="3031c-116">Use the default behavior if none of the other ILC\_COLORx flags is specified.</span></span> <span data-ttu-id="3031c-117">Normalmente, o padrão é ILC \_ COLOR4, mas para drivers de exibição mais antigos, o padrão é ILC \_ COLORDDB.</span><span class="sxs-lookup"><span data-stu-id="3031c-117">Typically, the default is ILC\_COLOR4, but for older display drivers, the default is ILC\_COLORDDB.</span></span><br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <span data-ttu-id="3031c-118"><dt>**ILC \_ COLORDDB**</dt> <dt>0x000000FE</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-118"><dt>**ILC\_COLORDDB**</dt> <dt>0x000000FE</dt></span></span> </dl>                         | <span data-ttu-id="3031c-119">Use um bitmap dependente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3031c-119">Use a device-dependent bitmap.</span></span><br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <span data-ttu-id="3031c-120"><dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-120"><dt>**ILC\_COLOR4**</dt> <dt>0x00000004</dt></span></span> </dl>                               | <span data-ttu-id="3031c-121">Use uma seção DIB (bitmap independente de dispositivo) de 4 bits (16 cores) como bitmap para a lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="3031c-121">Use a 4-bit (16-color) device-independent bitmap (DIB) section as the bitmap for the image list.</span></span><br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <span data-ttu-id="3031c-122"><dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-122"><dt>**ILC\_COLOR8**</dt> <dt>0x00000008</dt></span></span> </dl>                               | <span data-ttu-id="3031c-123">Use uma seção DIB de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="3031c-123">Use an 8-bit DIB section.</span></span> <span data-ttu-id="3031c-124">As cores usadas para a tabela de cores são as mesmas cores da paleta de meio-tom.</span><span class="sxs-lookup"><span data-stu-id="3031c-124">The colors used for the color table are the same colors as the halftone palette.</span></span><br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <span data-ttu-id="3031c-125"><dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-125"><dt>**ILC\_COLOR16**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="3031c-126">Use uma seção DIB de 16 bits (32/64k-Color).</span><span class="sxs-lookup"><span data-stu-id="3031c-126">Use a 16-bit (32/64k-color) DIB section.</span></span><br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <span data-ttu-id="3031c-127"><dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-127"><dt>**ILC\_COLOR24**</dt> <dt>0x00000018</dt></span></span> </dl>                            | <span data-ttu-id="3031c-128">Use uma seção DIB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="3031c-128">Use a 24-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <span data-ttu-id="3031c-129"><dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-129"><dt>**ILC\_COLOR32**</dt> <dt>0x00000020</dt></span></span> </dl>                            | <span data-ttu-id="3031c-130">Use uma seção DIB de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3031c-130">Use a 32-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <span data-ttu-id="3031c-131"><dt>**ILC \_**</dt> <dt>0X00000800</dt> da paleta</span><span class="sxs-lookup"><span data-stu-id="3031c-131"><dt>**ILC\_PALETTE**</dt> <dt>0x00000800</dt></span></span> </dl>                            | <span data-ttu-id="3031c-132">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="3031c-132">Not implemented.</span></span><br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <span data-ttu-id="3031c-133"><dt>**ILC \_**</dt> <dt>0X00002000</dt> de espelho</span><span class="sxs-lookup"><span data-stu-id="3031c-133"><dt>**ILC\_MIRROR**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="3031c-134">Espelhar os ícones contidos, se o processo for espelhado</span><span class="sxs-lookup"><span data-stu-id="3031c-134">Mirror the icons contained, if the process is mirrored</span></span><br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <span data-ttu-id="3031c-135"><dt>**ILC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-135"><dt>**ILC\_PERITEMMIRROR**</dt> <dt>0x00008000</dt></span></span> </dl>          | <span data-ttu-id="3031c-136">Faz com que o código de espelhamento espelhe cada item ao inserir um conjunto de imagens, em comparação com toda a faixa.</span><span class="sxs-lookup"><span data-stu-id="3031c-136">Causes the mirroring code to mirror each item when inserting a set of images, versus the whole strip.</span></span><br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <span data-ttu-id="3031c-137"><dt>**ILC \_ ORIGINALSIZE**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-137"><dt>**ILC\_ORIGINALSIZE**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="3031c-138">**Windows Vista e posterior.**</span><span class="sxs-lookup"><span data-stu-id="3031c-138">**Windows Vista and later.**</span></span> <span data-ttu-id="3031c-139">ImageList deve aceitar menor do que definir imagens e aplicar o tamanho original com base na imagem adicionada.</span><span class="sxs-lookup"><span data-stu-id="3031c-139">Imagelist should accept smaller than set images and apply original size based on image added.</span></span><br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <span data-ttu-id="3031c-140"><dt>**ILC \_ HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-140"><dt>**ILC\_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="3031c-141">**Windows Vista e posterior.**</span><span class="sxs-lookup"><span data-stu-id="3031c-141">**Windows Vista and later.**</span></span> <span data-ttu-id="3031c-142">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3031c-142">Reserved.</span></span><br/>                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="3031c-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3031c-143">Requirements</span></span>



| <span data-ttu-id="3031c-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3031c-144">Requirement</span></span> | <span data-ttu-id="3031c-145">Valor</span><span class="sxs-lookup"><span data-stu-id="3031c-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3031c-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3031c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3031c-147">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3031c-147">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3031c-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3031c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3031c-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3031c-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3031c-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3031c-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="3031c-151"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3031c-151"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





