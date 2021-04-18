---
description: Especifica o tamanho mínimo do pacote para um arquivo ASF, em bytes.
ms.assetid: 22e5725d-de55-4a0c-a6cc-1ed9f20e7663
title: Atributo MF_ASFPROFILE_MINPACKETSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8e1aaea4fe1dfc2c6e01e969bc8b588ac21e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781570"
---
# <a name="mf_asfprofile_minpacketsize-attribute"></a><span data-ttu-id="04bbb-103">\_Atributo MF ASFPROFILE \_ MINPACKETSIZE</span><span class="sxs-lookup"><span data-stu-id="04bbb-103">MF\_ASFPROFILE\_MINPACKETSIZE attribute</span></span>

<span data-ttu-id="04bbb-104">Especifica o tamanho mínimo do pacote para um arquivo ASF, em bytes.</span><span class="sxs-lookup"><span data-stu-id="04bbb-104">Specifies the minimum packet size for an ASF file, in bytes.</span></span>

## <a name="data-type"></a><span data-ttu-id="04bbb-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="04bbb-105">Data type</span></span>

<span data-ttu-id="04bbb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="04bbb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="04bbb-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="04bbb-107">Remarks</span></span>

<span data-ttu-id="04bbb-108">Esse atributo se aplica a objetos de perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="04bbb-108">This attribute applies to ASF profile objects.</span></span> <span data-ttu-id="04bbb-109">Para definir esse atributo, use a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="04bbb-109">To set this attribute, use the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>

<span data-ttu-id="04bbb-110">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="04bbb-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="04bbb-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04bbb-111">Requirements</span></span>



| <span data-ttu-id="04bbb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="04bbb-112">Requirement</span></span> | <span data-ttu-id="04bbb-113">Valor</span><span class="sxs-lookup"><span data-stu-id="04bbb-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04bbb-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04bbb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="04bbb-115">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04bbb-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="04bbb-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04bbb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="04bbb-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04bbb-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="04bbb-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04bbb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="04bbb-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="04bbb-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04bbb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="04bbb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bbb-121">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="04bbb-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="04bbb-122">Atributos ASF</span><span class="sxs-lookup"><span data-stu-id="04bbb-122">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="04bbb-123">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="04bbb-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="04bbb-124">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="04bbb-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




