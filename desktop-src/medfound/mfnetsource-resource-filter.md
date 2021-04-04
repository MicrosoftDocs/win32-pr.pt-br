---
description: Contém um ponteiro para a interface de retorno de chamada IMFNetResourceFilter para o fluxo de bytes HTTP Microsoft Media Foundation.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: Propriedade MFNETSOURCE_RESOURCE_FILTER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661571"
---
# <a name="mfnetsource_resource_filter-property"></a><span data-ttu-id="d0299-103">Propriedade de filtro de \_ recursos MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="d0299-103">MFNETSOURCE\_RESOURCE\_FILTER property</span></span>

<span data-ttu-id="d0299-104">Contém um ponteiro para a interface de retorno de chamada [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) para o fluxo de bytes http Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d0299-104">Contains a pointer to the [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) callback interface for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="d0299-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d0299-105">Data type</span></span>

<span data-ttu-id="d0299-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d0299-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d0299-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d0299-107">PROPVARIANT member</span></span>

<span data-ttu-id="d0299-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="d0299-108">\**IUnknown\** _</span></span>

<span data-ttu-id="d0299-109">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="d0299-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="d0299-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="d0299-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="d0299-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0299-111">Remarks</span></span>

<span data-ttu-id="d0299-112">Use essa propriedade para configurar o Media Foundation fluxo de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="d0299-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="d0299-113">Para definir a propriedade, passe um ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="d0299-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="d0299-114">Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="d0299-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0299-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0299-115">Requirements</span></span>



| <span data-ttu-id="d0299-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0299-116">Requirement</span></span> | <span data-ttu-id="d0299-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d0299-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0299-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0299-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d0299-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d0299-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d0299-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d0299-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d0299-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d0299-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d0299-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0299-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0299-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0299-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0299-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0299-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0299-125">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0299-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
