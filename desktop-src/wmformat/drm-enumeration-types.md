---
title: Tipos de enumeração de cliente Microsoft Windows Media DRM
description: Tipos de enumeração
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- SDK do Windows Media Format, tipos de enumeração
- DRM (gerenciamento de direitos digitais), tipos de enumeração
- DRM (gerenciamento de direitos digitais), tipos de enumeração
- APIs estendidas do cliente DRM, tipos de enumeração
- APIs estendidas do cliente, tipos de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c159342367035767d213d57987d93d23eb321a6c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008729"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="270fe-108">Tipos de enumeração de cliente Microsoft Windows Media DRM</span><span class="sxs-lookup"><span data-stu-id="270fe-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="270fe-109">A tabela a seguir descreve as enumerações que são suportadas pelas APIs estendidas do Microsoft Windows Media DRM Client.</span><span class="sxs-lookup"><span data-stu-id="270fe-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="270fe-110">Enumeração</span><span class="sxs-lookup"><span data-stu-id="270fe-110">Enumeration</span></span>                                                                      | <span data-ttu-id="270fe-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="270fe-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="270fe-112">**\_resultados de \_ \_ consulta permitidos \_ da ação DRM**</span><span class="sxs-lookup"><span data-stu-id="270fe-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="270fe-113">Usado pela interface [**IWMDRMLicenseQuery:: QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) para especificar o motivo pelo qual uma ação não é permitida.</span><span class="sxs-lookup"><span data-stu-id="270fe-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="270fe-114">**\_tipo de \_ dados attr DRM**</span><span class="sxs-lookup"><span data-stu-id="270fe-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="270fe-115">Define os tipos de dados usados para propriedades e atributos DRM.</span><span class="sxs-lookup"><span data-stu-id="270fe-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="270fe-116">**\_tipo de criptografia DRM \_**</span><span class="sxs-lookup"><span data-stu-id="270fe-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="270fe-117">Define os tipos de algoritmos criptográficos que podem ser usados para criptografar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="270fe-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="270fe-118">**\_status do http DRM \_**</span><span class="sxs-lookup"><span data-stu-id="270fe-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="270fe-119">Define um intervalo de Estados HTTP para uma solicitação de DRM.</span><span class="sxs-lookup"><span data-stu-id="270fe-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="270fe-120">**\_status de individualização de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="270fe-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="270fe-121">Define os Estados válidos para individualização de DRM.</span><span class="sxs-lookup"><span data-stu-id="270fe-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="270fe-122">**\_categoria de \_ estado da licença DRM \_**</span><span class="sxs-lookup"><span data-stu-id="270fe-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="270fe-123">Especifica o tipo de restrição de licença que é descrito por uma estrutura de [**\_ dados de \_ estado \_ de licença DRM**](drmdrm-license-state-data.md) .</span><span class="sxs-lookup"><span data-stu-id="270fe-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="270fe-124">**STATUS do MSDRM \_**</span><span class="sxs-lookup"><span data-stu-id="270fe-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="270fe-125">Define as condições de status do subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="270fe-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="270fe-126">**\_tipo de política WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="270fe-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="270fe-127">Lista os tipos de políticas que estão disponíveis para operações do Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="270fe-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="270fe-128">**direitos de WMT \_**</span><span class="sxs-lookup"><span data-stu-id="270fe-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="270fe-129">Define os direitos que podem ser especificados em uma licença DRM.</span><span class="sxs-lookup"><span data-stu-id="270fe-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="270fe-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="270fe-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="270fe-131">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="270fe-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




