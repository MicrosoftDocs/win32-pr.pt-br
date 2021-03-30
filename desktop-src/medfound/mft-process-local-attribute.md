---
description: Especifica se uma Media Foundation de transformação (MFT) é registrada somente no processo de aplicativos.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: Atributo MFT_PROCESS_LOCAL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661492"
---
# <a name="mft_process_local_attribute-attribute"></a><span data-ttu-id="e2929-103">\_Atributo de \_ atributo local do processo de MFT \_</span><span class="sxs-lookup"><span data-stu-id="e2929-103">MFT\_PROCESS\_LOCAL\_Attribute attribute</span></span>

<span data-ttu-id="e2929-104">Especifica se uma Media Foundation de transformação (MFT) é registrada somente no processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2929-104">Specifies whether a Media Foundation transform (MFT) is registered only in the application's process.</span></span>

## <a name="data-type"></a><span data-ttu-id="e2929-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e2929-105">Data type</span></span>

<span data-ttu-id="e2929-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e2929-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e2929-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="e2929-107">Get/set</span></span>

<span data-ttu-id="e2929-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e2929-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e2929-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e2929-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2929-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2929-110">Remarks</span></span>

<span data-ttu-id="e2929-111">Esse atributo é usado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e2929-111">This attribute is used as follows:</span></span>

1.  <span data-ttu-id="e2929-112">O aplicativo registra um MFT local chamando a função [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="e2929-112">The application registers a local MFT by calling either the [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) function.</span></span> <span data-ttu-id="e2929-113">Essas funções registram o MFT no processo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2929-113">These functions register the MFT in the application's process.</span></span>
2.  <span data-ttu-id="e2929-114">A função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) é chamada para enumerar MFTs que correspondem a um conjunto específico de critérios.</span><span class="sxs-lookup"><span data-stu-id="e2929-114">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function is called to enumerate MFTs that match a particular set of criteria.</span></span> <span data-ttu-id="e2929-115">O aplicativo pode chamar a função **MFTEnumEx** diretamente, mas, mais frequentemente, essa função é chamada pelo carregador de topologia.</span><span class="sxs-lookup"><span data-stu-id="e2929-115">The application might call the **MFTEnumEx** function directly, but more often this function is called by the topology loader.</span></span>
3.  <span data-ttu-id="e2929-116">A função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) recupera uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , cada um representando um objeto de ativação para um MFT.</span><span class="sxs-lookup"><span data-stu-id="e2929-116">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function retrieves an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each representing an activation object for an MFT.</span></span> <span data-ttu-id="e2929-117">Se uma MFT for registrada localmente, o \_ atributo local do processo de MFT \_ \_ será definido como **true** no objeto de ativação correspondente.</span><span class="sxs-lookup"><span data-stu-id="e2929-117">If an MFT is registered locally, the MFT\_PROCESS\_LOCAL\_Attribute attribute is set to **TRUE** on the corresponding activation object.</span></span>

<span data-ttu-id="e2929-118">O valor padrão para esse atributo é **false**.</span><span class="sxs-lookup"><span data-stu-id="e2929-118">The default value for this attribute is **FALSE**.</span></span>

<span data-ttu-id="e2929-119">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e2929-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2929-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2929-120">Requirements</span></span>



| <span data-ttu-id="e2929-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2929-121">Requirement</span></span> | <span data-ttu-id="e2929-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e2929-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2929-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2929-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e2929-124">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e2929-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e2929-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2929-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e2929-126">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e2929-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e2929-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2929-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2929-128"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2929-128"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2929-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2929-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2929-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2929-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2929-131">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="e2929-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




