---
description: Especifica se o MFT do remux de vídeo H. 264 deve marcar I imagens como ponto de limpeza para melhor capacidade de busca. Isso tem o potencial de danos em buscas em arquivos MP4 finais em não conformidade.
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: Atributo MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789250"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a><span data-ttu-id="c2dc8-104">MFT \_ remux \_ Marcar \_ \_ \_ como atributo de \_ \_ ponto limpo</span><span class="sxs-lookup"><span data-stu-id="c2dc8-104">MFT\_REMUX\_MARK\_I\_PICTURE\_AS\_CLEAN\_POINT attribute</span></span>

<span data-ttu-id="c2dc8-105">Especifica se o MFT do remux de vídeo H. 264 deve marcar I imagens como ponto de limpeza para melhor capacidade de busca.</span><span class="sxs-lookup"><span data-stu-id="c2dc8-105">Specifies whether the H.264 video remux MFT should mark I pictures as clean point for better seek-ability.</span></span> <span data-ttu-id="c2dc8-106">Isso tem o potencial de danos em buscas em arquivos MP4 finais em não conformidade.</span><span class="sxs-lookup"><span data-stu-id="c2dc8-106">This has the potential for corruptions on seeks in non-conforming final MP4 files.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2dc8-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c2dc8-107">Data type</span></span>

<span data-ttu-id="c2dc8-108">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c2dc8-108">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c2dc8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2dc8-109">Remarks</span></span>

<span data-ttu-id="c2dc8-110">A imagem do ponto de limpeza deve ser compactada com imagens IDR por definição.</span><span class="sxs-lookup"><span data-stu-id="c2dc8-110">Clean point picture should be compressed IDR pictures by definition.</span></span>

<span data-ttu-id="c2dc8-111">Isso não é recomendado para gravar ou remuxing arquivos MP4, a menos que esse exercício seja produzir alguns arquivos pseudo MP4 intermediários para edição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2dc8-111">This is not recommended for recording or remuxing MP4 files, unless such an exercise is to produce some intermediate pseudo MP4 files for video editing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2dc8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2dc8-112">Requirements</span></span>



| <span data-ttu-id="c2dc8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2dc8-113">Requirement</span></span> | <span data-ttu-id="c2dc8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c2dc8-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2dc8-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2dc8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c2dc8-116">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c2dc8-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c2dc8-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2dc8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c2dc8-118">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c2dc8-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="c2dc8-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2dc8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2dc8-120"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2dc8-120"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2dc8-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="c2dc8-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2dc8-122"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2dc8-122"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2dc8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2dc8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2dc8-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c2dc8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




