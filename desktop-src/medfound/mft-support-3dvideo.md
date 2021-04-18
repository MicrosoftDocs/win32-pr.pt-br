---
description: Especifica se uma Media Foundation transformação (MFT) dá suporte ao vídeo 3D estereoscópico.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Atributo MFT_SUPPORT_3DVIDEO (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810843"
---
# <a name="mft_support_3dvideo-attribute"></a><span data-ttu-id="114db-103">Suporte de MFT \_ \_ atributo 3DVIDEO</span><span class="sxs-lookup"><span data-stu-id="114db-103">MFT\_SUPPORT\_3DVIDEO attribute</span></span>

<span data-ttu-id="114db-104">Especifica se uma Media Foundation transformação (MFT) dá suporte ao vídeo 3D estereoscópico.</span><span class="sxs-lookup"><span data-stu-id="114db-104">Specifies whether a Media Foundation transform (MFT) supports 3D stereoscopic video.</span></span>

## <a name="data-type"></a><span data-ttu-id="114db-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="114db-105">Data type</span></span>

<span data-ttu-id="114db-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="114db-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="114db-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="114db-107">Remarks</span></span>

<span data-ttu-id="114db-108">Para consultar esse atributo, chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributo global do MFT.</span><span class="sxs-lookup"><span data-stu-id="114db-108">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="114db-109">Se **GetAttributes** tiver sucesso, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="114db-109">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="114db-110">O valor padrão desse atributo é **false**.</span><span class="sxs-lookup"><span data-stu-id="114db-110">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="114db-111">Trate este atributo como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="114db-111">Treat this attribute as read-only.</span></span> <span data-ttu-id="114db-112">Não altere o valor; o MFT ignorará as alterações no valor.</span><span class="sxs-lookup"><span data-stu-id="114db-112">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="114db-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="114db-113">Requirements</span></span>



| <span data-ttu-id="114db-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="114db-114">Requirement</span></span> | <span data-ttu-id="114db-115">Valor</span><span class="sxs-lookup"><span data-stu-id="114db-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="114db-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="114db-116">Minimum supported client</span></span><br/> | <span data-ttu-id="114db-117">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="114db-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="114db-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="114db-118">Minimum supported server</span></span><br/> | <span data-ttu-id="114db-119">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="114db-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="114db-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="114db-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="114db-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="114db-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="114db-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="114db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="114db-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="114db-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




