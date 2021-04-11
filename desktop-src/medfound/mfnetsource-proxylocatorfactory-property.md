---
description: Contém um ponteiro para a interface IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: Propriedade MFNETSOURCE_PROXYLOCATORFACTORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091152"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a><span data-ttu-id="a9111-103">\_Propriedade MFNETSOURCE PROXYLOCATORFACTORY</span><span class="sxs-lookup"><span data-stu-id="a9111-103">MFNETSOURCE\_PROXYLOCATORFACTORY property</span></span>

<span data-ttu-id="a9111-104">Contém um ponteiro para a interface [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="a9111-104">Contains a pointer to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>



<span data-ttu-id="a9111-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a9111-105">Data type</span></span>

<span data-ttu-id="a9111-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a9111-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a9111-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a9111-107">PROPVARIANT member</span></span>

<span data-ttu-id="a9111-108">Ponteiro **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="a9111-108">**IUnknown** pointer</span></span>

<span data-ttu-id="a9111-109">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="a9111-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="a9111-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="a9111-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a9111-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9111-111">Remarks</span></span>

<span data-ttu-id="a9111-112">A constante **MFNETSOURCE \_ PROXYLOCATORFACTORY** define o GUID para essa chave de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a9111-112">The constant **MFNETSOURCE\_PROXYLOCATORFACTORY** defines the GUID for this property key.</span></span> <span data-ttu-id="a9111-113">O identificador de propriedade (PID) é zero.</span><span class="sxs-lookup"><span data-stu-id="a9111-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="a9111-114">Os aplicativos podem usar essa propriedade para fornecer um localizador de proxy personalizado para a origem da rede.</span><span class="sxs-lookup"><span data-stu-id="a9111-114">Applications can use this property to provide a custom proxy locator for the network source.</span></span> <span data-ttu-id="a9111-115">Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="a9111-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="a9111-116">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a9111-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9111-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9111-117">Requirements</span></span>



| <span data-ttu-id="a9111-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9111-118">Requirement</span></span> | <span data-ttu-id="a9111-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a9111-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9111-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9111-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a9111-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9111-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a9111-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9111-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a9111-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a9111-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a9111-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9111-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9111-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9111-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9111-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9111-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9111-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9111-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a9111-128">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9111-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a9111-129">Suporte de proxy para fontes de rede</span><span class="sxs-lookup"><span data-stu-id="a9111-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




