---
description: Especifica como o coletor de mídia ASF deve aplicar o DRM do Windows Media.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: Propriedade MFPKEY_ASFMEDIASINK_DRMACTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663815"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a><span data-ttu-id="4f317-103">\_Propriedade MFPKEY ASFMEDIASINK \_ DRMACTION</span><span class="sxs-lookup"><span data-stu-id="4f317-103">MFPKEY\_ASFMEDIASINK\_DRMACTION property</span></span>

<span data-ttu-id="4f317-104">Especifica como o coletor de mídia ASF deve aplicar o DRM do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4f317-104">Specifies how the ASF media sink should apply Windows Media DRM.</span></span>



<span data-ttu-id="4f317-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4f317-105">Data type</span></span>

<span data-ttu-id="4f317-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="4f317-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4f317-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="4f317-107">PROPVARIANT member</span></span>

<span data-ttu-id="4f317-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="4f317-108">**ULONG**</span></span>

<span data-ttu-id="4f317-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="4f317-109">VT\_UI4</span></span>

<span data-ttu-id="4f317-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="4f317-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4f317-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f317-111">Remarks</span></span>

<span data-ttu-id="4f317-112">O valor dessa propriedade é um membro da enumeração [**MFSINK \_ WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) .</span><span class="sxs-lookup"><span data-stu-id="4f317-112">The value of this property is a member of the [**MFSINK\_WMDRMACTION**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) enumeration.</span></span>

<span data-ttu-id="4f317-113">Você pode usar esse atributo para configurar o coletor de mídia ASF.</span><span class="sxs-lookup"><span data-stu-id="4f317-113">You can use this attribute to configure the ASF media sink.</span></span> <span data-ttu-id="4f317-114">O uso depende de qual função você chama para criar o coletor de mídia ASF:</span><span class="sxs-lookup"><span data-stu-id="4f317-114">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="4f317-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): consulta o ponteiro [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) recuperado para a interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="4f317-115">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="4f317-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) no ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) especificado no parâmetro *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="4f317-116">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f317-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f317-117">Requirements</span></span>



| <span data-ttu-id="4f317-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f317-118">Requirement</span></span> | <span data-ttu-id="4f317-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4f317-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f317-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f317-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4f317-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f317-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4f317-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f317-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4f317-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f317-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4f317-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f317-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f317-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f317-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f317-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f317-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f317-127">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4f317-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
