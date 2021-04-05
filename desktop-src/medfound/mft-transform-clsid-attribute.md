---
description: Contém o identificador de classe (CLSID) de uma Media Foundation de transformação (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: Atributo MFT_TRANSFORM_CLSID_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921218"
---
# <a name="mft_transform_clsid_attribute-attribute"></a><span data-ttu-id="78473-103">\_Atributo de \_ atributo CLSID de transformação de MFT \_</span><span class="sxs-lookup"><span data-stu-id="78473-103">MFT\_TRANSFORM\_CLSID\_Attribute attribute</span></span>

<span data-ttu-id="78473-104">Contém o identificador de classe (CLSID) de uma Media Foundation de transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="78473-104">Contains the class identifier (CLSID) of a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="78473-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="78473-105">Data type</span></span>

<span data-ttu-id="78473-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="78473-106">**GUID**</span></span>

## <a name="getset"></a><span data-ttu-id="78473-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="78473-107">Get/set</span></span>

<span data-ttu-id="78473-108">Para obter esse atributo, chame [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="78473-108">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="78473-109">Para definir esse atributo, chame [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="78473-109">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="78473-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="78473-110">Remarks</span></span>

<span data-ttu-id="78473-111">Esse atributo é definido nos ponteiros do [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="78473-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="78473-112">Esse atributo é usado internamente pelo objeto de ativação quando cria o MFT.</span><span class="sxs-lookup"><span data-stu-id="78473-112">This attribute is used internally by the activation object when it creates the MFT.</span></span> <span data-ttu-id="78473-113">Os aplicativos não devem usar esse CLSID diretamente para criar o MFT, pois o objeto de ativação pode precisar inicializar o MFT.</span><span class="sxs-lookup"><span data-stu-id="78473-113">Applications should not use this CLSID directly to create the MFT, because the activation object might need to initialize the MFT.</span></span> <span data-ttu-id="78473-114">Portanto, para criar uma instância do MFT, chame [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no objeto Activation.</span><span class="sxs-lookup"><span data-stu-id="78473-114">Therefore, to create an instance of the MFT, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the activation object.</span></span>

<span data-ttu-id="78473-115">Observe que a função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporta de maneira diferente da função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) nesse sentido.</span><span class="sxs-lookup"><span data-stu-id="78473-115">Note that the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function behaves differently than the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function in this respect.</span></span> <span data-ttu-id="78473-116">A função **MFTEnum** retorna CLSIDs, que o aplicativo passa para a função **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="78473-116">The **MFTEnum** function returns CLSIDs, which the application passes to the **CoCreateInstance** function.</span></span> <span data-ttu-id="78473-117">A função **MFTEnumEx** retorna objetos de ativação em vez de CLSIDs.</span><span class="sxs-lookup"><span data-stu-id="78473-117">The **MFTEnumEx** function returns activation objects rather than CLSIDs.</span></span>

<span data-ttu-id="78473-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="78473-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="78473-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78473-119">Requirements</span></span>



| <span data-ttu-id="78473-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="78473-120">Requirement</span></span> | <span data-ttu-id="78473-121">Valor</span><span class="sxs-lookup"><span data-stu-id="78473-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="78473-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78473-122">Minimum supported client</span></span><br/> | <span data-ttu-id="78473-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="78473-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="78473-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78473-124">Minimum supported server</span></span><br/> | <span data-ttu-id="78473-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="78473-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="78473-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78473-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="78473-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="78473-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78473-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="78473-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78473-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="78473-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="78473-130">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="78473-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




