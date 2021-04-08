---
description: Contém propriedades de configuração para um codificador.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: Atributo MFT_PREFERRED_ENCODER_PROFILE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921219"
---
# <a name="mft_preferred_encoder_profile-attribute"></a><span data-ttu-id="cfd20-103">\_Atributo de \_ perfil de codificador de MFT preferencial \_</span><span class="sxs-lookup"><span data-stu-id="cfd20-103">MFT\_PREFERRED\_ENCODER\_PROFILE attribute</span></span>

<span data-ttu-id="cfd20-104">Contém propriedades de configuração para um codificador.</span><span class="sxs-lookup"><span data-stu-id="cfd20-104">Contains configuration properties for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="cfd20-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cfd20-105">Data type</span></span>

<span data-ttu-id="cfd20-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ armazenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="cfd20-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="cfd20-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="cfd20-107">Get/set</span></span>

<span data-ttu-id="cfd20-108">Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="cfd20-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="cfd20-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="cfd20-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="cfd20-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="cfd20-110">Applies to</span></span>

[<span data-ttu-id="cfd20-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="cfd20-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="cfd20-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfd20-112">Remarks</span></span>

<span data-ttu-id="cfd20-113">Esse atributo pode ser definido no objeto de ativação retornado pela função [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="cfd20-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="cfd20-114">O atributo se aplica somente quando o objeto de ativação é configurado para criar um codificador.</span><span class="sxs-lookup"><span data-stu-id="cfd20-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="cfd20-115">O valor do atributo é um ponteiro para um repositório de atributos, que contém propriedades a serem definidas no codificador.</span><span class="sxs-lookup"><span data-stu-id="cfd20-115">The value of the attribute is a pointer to an attribute store, which itself contains properties to set on the encoder.</span></span>

<span data-ttu-id="cfd20-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cfd20-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd20-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfd20-117">Requirements</span></span>



| <span data-ttu-id="cfd20-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfd20-118">Requirement</span></span> | <span data-ttu-id="cfd20-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cfd20-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd20-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfd20-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfd20-121">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cfd20-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="cfd20-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfd20-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfd20-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="cfd20-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cfd20-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfd20-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfd20-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfd20-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd20-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfd20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd20-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cfd20-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cfd20-128">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="cfd20-128">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="cfd20-129">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="cfd20-129">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




