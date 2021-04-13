---
description: Especifica se o leitor de origem habilita a DXVA (aceleração de vídeo do DirectX) no decodificador de vídeo.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: Atributo MF_SOURCE_READER_DISABLE_DXVA (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297396"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a><span data-ttu-id="7f619-103">\_Leitor de origem MF \_ \_ desabilitar \_ atributo DXVA</span><span class="sxs-lookup"><span data-stu-id="7f619-103">MF\_SOURCE\_READER\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="7f619-104">Especifica se o [leitor de origem](source-reader.md) HABILITA a DXVA (aceleração de vídeo do DirectX) no decodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7f619-104">Specifies whether the [Source Reader](source-reader.md) enables DirectX Video Acceleration (DXVA) on the video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f619-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7f619-105">Data type</span></span>

<span data-ttu-id="7f619-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f619-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7f619-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="7f619-107">Get/set</span></span>

<span data-ttu-id="7f619-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7f619-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7f619-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7f619-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f619-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f619-110">Remarks</span></span>

<span data-ttu-id="7f619-111">Esse atributo se aplicará se as seguintes condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="7f619-111">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="7f619-112">O leitor de origem decodifica um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7f619-112">The source reader decodes a video stream.</span></span>
-   <span data-ttu-id="7f619-113">O decodificador de vídeo dá suporte à decodificação de DXVA.</span><span class="sxs-lookup"><span data-stu-id="7f619-113">The video decoder supports DXVA decoding.</span></span>
-   <span data-ttu-id="7f619-114">O aplicativo usa o atributo de Gerenciador de [ \_ leitura de leitor de origem \_ \_ \_ MF](mf-source-reader-d3d-manager.md) para definir o [Direct3D gerenciador de dispositivos](direct3d-device-manager.md) no leitor de origem.</span><span class="sxs-lookup"><span data-stu-id="7f619-114">The application uses the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute to set the [Direct3D Device Manager](direct3d-device-manager.md) on the source reader.</span></span>

<span data-ttu-id="7f619-115">Esse atributo permite que o aplicativo desabilite o DXVA enquanto estiver decodificando as superfícies do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7f619-115">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="7f619-116">Por padrão, o leitor de origem usa o [Gerenciador de dispositivos Direct3D](direct3d-device-manager.md) para duas finalidades:</span><span class="sxs-lookup"><span data-stu-id="7f619-116">By default, the source reader uses the [Direct3D Device Manager](direct3d-device-manager.md) for two purposes:</span></span>

-   <span data-ttu-id="7f619-117">Para habilitar a decodificação de DXVA no decodificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7f619-117">To enable DXVA decoding in the video decoder.</span></span>
-   <span data-ttu-id="7f619-118">Para alocar superfícies do Direct3D para os exemplos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7f619-118">To allocate Direct3D surfaces for the video samples.</span></span>

<span data-ttu-id="7f619-119">Se o valor do leitor de \_ origem \_ MF \_ desabilitar o \_ atributo DXVA for **true**, o leitor de origem desabilita a decodificação de dxva, embora ainda use o [Gerenciador de dispositivos Direct3D](direct3d-device-manager.md) para alocar superfícies Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7f619-119">If the value of the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is **TRUE**, the source reader does disables DXVA decoding, although it still uses the [Direct3D Device Manager](direct3d-device-manager.md) to allocate Direct3D surfaces.</span></span>

<span data-ttu-id="7f619-120">Se o [atributo \_ \_ \_ \_ Gerenciador D3D do leitor de origem MF](mf-source-reader-d3d-manager.md) não estiver definido, o \_ atributo DXVA desabilitar o leitor de origem MF \_ \_ \_ será ignorado.</span><span class="sxs-lookup"><span data-stu-id="7f619-120">If the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute is not set, the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is ignored.</span></span>

<span data-ttu-id="7f619-121">O valor padrão desse atributo é **false**, o que significa que a decodificação de DXVA está habilitada quando disponível.</span><span class="sxs-lookup"><span data-stu-id="7f619-121">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f619-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f619-122">Requirements</span></span>



| <span data-ttu-id="7f619-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f619-123">Requirement</span></span> | <span data-ttu-id="7f619-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7f619-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f619-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f619-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7f619-126">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7f619-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="7f619-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f619-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7f619-128">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="7f619-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7f619-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f619-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f619-130"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f619-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f619-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f619-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f619-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f619-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f619-133">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="7f619-133">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="7f619-134">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="7f619-134">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




