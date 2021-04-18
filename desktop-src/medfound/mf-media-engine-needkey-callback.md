---
description: O atributo que é passado no IMFMediaEngineNeedKeyNotify para o mecanismo de mídia na criação.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: MF_MEDIA_ENGINE_NEEDKEY_CALLBACK atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763916"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a><span data-ttu-id="39776-103">\_Atributo de \_ retorno de \_ chamada NEEDKEY do mecanismo de mídia MF \_</span><span class="sxs-lookup"><span data-stu-id="39776-103">MF\_MEDIA\_ENGINE\_NEEDKEY\_CALLBACK attribute</span></span>

<span data-ttu-id="39776-104">O atributo que é passado no [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) para o mecanismo de mídia na criação.</span><span class="sxs-lookup"><span data-stu-id="39776-104">Attribute which is passed in the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) to the media engine on creation.</span></span>

## <a name="data-type"></a><span data-ttu-id="39776-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="39776-105">Data type</span></span>

<span data-ttu-id="39776-106">**IMFMediaEngineNeedKeyNotify \* *_ armazenado como _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="39776-106">**IMFMediaEngineNeedKeyNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="39776-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="39776-107">Get/set</span></span>

<span data-ttu-id="39776-108">Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="39776-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="39776-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="39776-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="39776-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="39776-110">Remarks</span></span>

<span data-ttu-id="39776-111">O valor desse atributo é um ponteiro para a interface [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , implementado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39776-111">The value of this attribute is a pointer to the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) interface, implemented by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="39776-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39776-112">Requirements</span></span>



| <span data-ttu-id="39776-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="39776-113">Requirement</span></span> | <span data-ttu-id="39776-114">Valor</span><span class="sxs-lookup"><span data-stu-id="39776-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39776-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39776-115">Minimum supported client</span></span><br/> | <span data-ttu-id="39776-116">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39776-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="39776-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39776-117">Minimum supported server</span></span><br/> | <span data-ttu-id="39776-118">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="39776-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="39776-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="39776-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39776-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39776-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39776-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="39776-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39776-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39776-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




