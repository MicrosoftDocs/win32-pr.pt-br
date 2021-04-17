---
title: Lista de atributos DRM
description: Lista de atributos DRM
ms.assetid: 222ef91c-b776-4de8-b1ad-88c2beca05aa
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, DRM (gerenciamento de direitos digitais)
- DRM (gerenciamento de direitos digitais), atributos
- DRM (gerenciamento de direitos digitais), atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3beccc33a48f57015040f06c140a55f5f9691daa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798269"
---
# <a name="drm-attribute-list"></a><span data-ttu-id="d891b-109">Lista de atributos DRM</span><span class="sxs-lookup"><span data-stu-id="d891b-109">DRM Attribute List</span></span>

<span data-ttu-id="d891b-110">Para sua conveniência, a tabela a seguir lista todos os atributos de arquivo relacionados ao DRM.</span><span class="sxs-lookup"><span data-stu-id="d891b-110">For convenience, the following table lists all the DRM-related file attributes.</span></span> <span data-ttu-id="d891b-111">(Esses atributos também estão listados na tabela de todos os atributos na [lista de atributos](attribute-list.md).)</span><span class="sxs-lookup"><span data-stu-id="d891b-111">(These attributes are also listed in the table of all attributes under [Attribute List](attribute-list.md).)</span></span>

<span data-ttu-id="d891b-112">Os aplicativos podem definir esses valores ao gravar arquivos DRM e podem recuperá-los durante a leitura.</span><span class="sxs-lookup"><span data-stu-id="d891b-112">Applications can set these values when writing DRM files and can retrieve them when reading.</span></span>



| <span data-ttu-id="d891b-113">Atributo de arquivo DRM</span><span class="sxs-lookup"><span data-stu-id="d891b-113">DRM file attribute</span></span>                                                                   | <span data-ttu-id="d891b-114">Identificador global</span><span class="sxs-lookup"><span data-stu-id="d891b-114">Global identifier</span></span>                             | <span data-ttu-id="d891b-115">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d891b-115">Data type</span></span>             |
|--------------------------------------------------------------------------------------|-----------------------------------------------|-----------------------|
| [<span data-ttu-id="d891b-116">**\_ContentId DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-116">**DRM\_ContentID**</span></span>](drm-contentid.md)                                              | <span data-ttu-id="d891b-117">g \_ wszWMDRM \_ ContentId</span><span class="sxs-lookup"><span data-stu-id="d891b-117">g\_wszWMDRM\_ContentID</span></span>                        | <span data-ttu-id="d891b-118">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-118">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-119">**\_ContentDistributor DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-119">**DRM\_DRMHeader\_ContentDistributor**</span></span>](drm-drmheader-contentdistributor.md)       | <span data-ttu-id="d891b-120">g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="d891b-120">g\_wszWMDRM\_DRMHeader\_ContentDistributor</span></span>    | <span data-ttu-id="d891b-121">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-121">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-122">**\_ContentId do DRM DRMHeader \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-122">**DRM\_DRMHeader\_ContentID**</span></span>](drm-drmheader-contentid.md)                         | <span data-ttu-id="d891b-123">g \_ wszWMDRM \_ DRMHeader \_ ContentId</span><span class="sxs-lookup"><span data-stu-id="d891b-123">g\_wszWMDRM\_DRMHeader\_ContentID</span></span>             | <span data-ttu-id="d891b-124">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-124">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-125">**\_IndividualizedVersion DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-125">**DRM\_DRMHeader\_IndividualizedVersion**</span></span>](drm-drmheader-individualizedversion.md) | <span data-ttu-id="d891b-126">g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="d891b-126">g\_wszWMDRM\_DRMHeader\_IndividualizedVersion</span></span> | <span data-ttu-id="d891b-127">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-127">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-128">**\_Keyid DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-128">**DRM\_DRMHeader\_KeyID**</span></span>](drm-drmheader-keyid.md)                                 | <span data-ttu-id="d891b-129">\_keyid g wszWMDRM \_ DRMHeader \_</span><span class="sxs-lookup"><span data-stu-id="d891b-129">g\_wszWMDRM\_DRMHeader\_KeyID</span></span>                 | <span data-ttu-id="d891b-130">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-130">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-131">**\_LicenseAcqURL DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-131">**DRM\_DRMHeader\_LicenseAcqURL**</span></span>](drm-drmheader-licenseacqurl.md)                 | <span data-ttu-id="d891b-132">g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="d891b-132">g\_wszWMDRM\_DRMHeader\_LicenseAcqURL</span></span>         | <span data-ttu-id="d891b-133">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-133">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-134">**\_SubscriptionContentID DRMHEADER \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-134">**DRM\_DRMHeader\_SubscriptionContentID**</span></span>](drm-drmheader-subscriptioncontentid.md) | <span data-ttu-id="d891b-135">g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID</span><span class="sxs-lookup"><span data-stu-id="d891b-135">g\_wszWMDRM\_DRMHeader\_SubscriptionContentID</span></span> | <span data-ttu-id="d891b-136">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-136">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-137">**\_DRMHEADER DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-137">**DRM\_DRMHeader**</span></span>](drm-drmheader.md)                                              | <span data-ttu-id="d891b-138">g \_ wszWMDRM \_ DRMHeader</span><span class="sxs-lookup"><span data-stu-id="d891b-138">g\_wszWMDRM\_DRMHeader</span></span>                        | <span data-ttu-id="d891b-139">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-139">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-140">**\_INDIVIDUALIZEDVERSION DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-140">**DRM\_IndividualizedVersion**</span></span>](drm-individualizedversion.md)                      | <span data-ttu-id="d891b-141">g \_ wszWMDRM \_ IndividualizedVersion</span><span class="sxs-lookup"><span data-stu-id="d891b-141">g\_wszWMDRM\_IndividualizedVersion</span></span>            | <span data-ttu-id="d891b-142">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-142">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-143">**\_Keyid DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-143">**DRM\_KeyID**</span></span>](drm-keyid.md)                                                      | <span data-ttu-id="d891b-144">\_keyid g wszWMDRM \_</span><span class="sxs-lookup"><span data-stu-id="d891b-144">g\_wszWMDRM\_KeyID</span></span>                            | <span data-ttu-id="d891b-145">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-145">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-146">**\_LASIGNATURECERT DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-146">**DRM\_LASignatureCert**</span></span>](drm-lasignaturecert.md)                                  | <span data-ttu-id="d891b-147">g \_ wszWMDRM \_ LASignatureCert</span><span class="sxs-lookup"><span data-stu-id="d891b-147">g\_wszWMDRM\_LASignatureCert</span></span>                  | <span data-ttu-id="d891b-148">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-148">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-149">**\_LASIGNATURELICSRVCERT DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-149">**DRM\_LASignatureLicSrvCert**</span></span>](drm-lasignaturelicsrvcert.md)                      | <span data-ttu-id="d891b-150">g \_ wszWMDRM \_ LASignatureLicSrvCert</span><span class="sxs-lookup"><span data-stu-id="d891b-150">g\_wszWMDRM\_LASignatureLicSrvCert</span></span>            | <span data-ttu-id="d891b-151">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-151">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-152">**\_LASIGNATUREPRIVKEY DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-152">**DRM\_LASignaturePrivKey**</span></span>](drm-lasignatureprivkey.md)                            | <span data-ttu-id="d891b-153">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="d891b-153">g\_wszWMDRM\_LASignaturePrivKey</span></span>               | <span data-ttu-id="d891b-154">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-154">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-155">**\_LASIGNATUREROOTCERT DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-155">**DRM\_LASignatureRootCert**</span></span>](drm-lasignaturerootcert.md)                          | <span data-ttu-id="d891b-156">g \_ wszWMDRM \_ LASignatureRootCert</span><span class="sxs-lookup"><span data-stu-id="d891b-156">g\_wszWMDRM\_LASignatureRootCert</span></span>              | <span data-ttu-id="d891b-157">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-157">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-158">**\_LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-158">**DRM\_LicenseAcqURL**</span></span>](drm-licenseacqurl.md)                                      | <span data-ttu-id="d891b-159">g \_ wszWMDRM \_ LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="d891b-159">g\_wszWMDRM\_LicenseAcqURL</span></span>                    | <span data-ttu-id="d891b-160">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-160">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="d891b-161">**\_V1LICENSEACQURL DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-161">**DRM\_V1LicenseAcqURL**</span></span>](drm-v1licenseacqurl.md)                                  | <span data-ttu-id="d891b-162">g \_ wszWMDRM \_ V1LicenseAcqURL</span><span class="sxs-lookup"><span data-stu-id="d891b-162">g\_wszWMDRM\_V1LicenseAcqURL</span></span>                  | <span data-ttu-id="d891b-163">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="d891b-163">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d891b-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d891b-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d891b-165">**Atributos por tipo**</span><span class="sxs-lookup"><span data-stu-id="d891b-165">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="d891b-166">**Propriedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="d891b-166">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




