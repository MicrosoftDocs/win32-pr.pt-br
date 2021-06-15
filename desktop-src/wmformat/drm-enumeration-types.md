---
title: Tipos de enumeração de cliente DRM da Mídia do Microsoft Windows
description: Saiba mais sobre as enumerações com suporte nas APIs Estendidas do Cliente DRM do Microsoft Windows Media.
ms.assetid: 940f66e1-1dc1-414f-bba9-b91f4f0dfc45
keywords:
- Windows Media Format SDK, tipos de enumeração
- DRM (gerenciamento de direitos digitais), tipos de enumeração
- DRM (gerenciamento de direitos digitais), tipos de enumeração
- APIs estendidas do cliente DRM, tipos de enumeração
- APIs estendidas do cliente, tipos de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574136f8016161f4d2c208865a72ad2a86d98f68
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068423"
---
# <a name="microsoft-windows-media-drm-client-enumeration-types"></a><span data-ttu-id="355c8-108">Tipos de enumeração de cliente DRM da Mídia do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="355c8-108">Microsoft Windows Media DRM Client Enumeration Types</span></span>

<span data-ttu-id="355c8-109">A tabela a seguir descreve as enumerações com suporte nas APIs Estendidas do Cliente DRM da Mídia do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="355c8-109">The following table describes the enumerations that are supported by the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="355c8-110">Enumeração</span><span class="sxs-lookup"><span data-stu-id="355c8-110">Enumeration</span></span>                                                                      | <span data-ttu-id="355c8-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="355c8-111">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="355c8-112">**A AÇÃO DRM \_ \_ PERMITIU RESULTADOS DA \_ \_ CONSULTA**</span><span class="sxs-lookup"><span data-stu-id="355c8-112">**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**</span></span>](drm-action-allowed-query-results.md) | <span data-ttu-id="355c8-113">Usado pela interface [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) para especificar o motivo pelo qual uma ação não é permitida.</span><span class="sxs-lookup"><span data-stu-id="355c8-113">Used by the [**IWMDRMLicenseQuery::QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) interface to specify the reason an action is not allowed.</span></span> |
| [<span data-ttu-id="355c8-114">**DRM \_ ATTR \_ DATATYPE**</span><span class="sxs-lookup"><span data-stu-id="355c8-114">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)                                 | <span data-ttu-id="355c8-115">Define os tipos de dados usados para propriedades e atributos drm.</span><span class="sxs-lookup"><span data-stu-id="355c8-115">Defines the data types used for DRM attributes and properties.</span></span>                                                                                                |
| [<span data-ttu-id="355c8-116">**TIPO DE CRIPTOGRAFIA DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="355c8-116">**DRM\_CRYPTO\_TYPE**</span></span>](drm-crypto-type.md)                                     | <span data-ttu-id="355c8-117">Define os tipos de algoritmo criptográfico que podem ser usados para criptografar conteúdo.</span><span class="sxs-lookup"><span data-stu-id="355c8-117">Defines the cryptographic algorithm types that can be used to encrypt content.</span></span>                                                                                |
| [<span data-ttu-id="355c8-118">**STATUS \_ HTTP DO DRM \_**</span><span class="sxs-lookup"><span data-stu-id="355c8-118">**DRM\_HTTP\_STATUS**</span></span>](drmdrm-http-status.md)                                  | <span data-ttu-id="355c8-119">Define um intervalo de estados HTTP para uma solicitação DRM.</span><span class="sxs-lookup"><span data-stu-id="355c8-119">Defines a range of HTTP states for a DRM request.</span></span>                                                                                                             |
| [<span data-ttu-id="355c8-120">**STATUS DE INDIVIDUALIZAÇÃO DO DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="355c8-120">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drmdrm-individualization-status.md)        | <span data-ttu-id="355c8-121">Define os estados válidos para individualização de DRM.</span><span class="sxs-lookup"><span data-stu-id="355c8-121">Defines the valid states for DRM individualization.</span></span>                                                                                                           |
| [<span data-ttu-id="355c8-122">**CATEGORIA DE ESTADO \_ DA \_ LICENÇA DRM \_**</span><span class="sxs-lookup"><span data-stu-id="355c8-122">**DRM\_LICENSE\_STATE\_CATEGORY**</span></span>](drmdrm-license-state-category.md)           | <span data-ttu-id="355c8-123">Especifica o tipo de restrição de licença descrito por uma estrutura [**DE DADOS DE ESTADO DE LICENÇA \_ \_ \_ DRM.**](drmdrm-license-state-data.md)</span><span class="sxs-lookup"><span data-stu-id="355c8-123">Specifies the type of license restriction that is described by a [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structure.</span></span>                    |
| [<span data-ttu-id="355c8-124">**STATUS DO MSDRM \_**</span><span class="sxs-lookup"><span data-stu-id="355c8-124">**MSDRM\_STATUS**</span></span>](msdrm-status.md)                                            | <span data-ttu-id="355c8-125">Define condições de status para o subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="355c8-125">Defines status conditions for the DRM subsystem.</span></span>                                                                                                              |
| [<span data-ttu-id="355c8-126">**TIPO DE POLÍTICA WMDRMNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="355c8-126">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)                           | <span data-ttu-id="355c8-127">Lista os tipos de políticas disponíveis para operações de DRM de Mídia do Windows para Dispositivos de Rede.</span><span class="sxs-lookup"><span data-stu-id="355c8-127">Lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>                                                          |
| [<span data-ttu-id="355c8-128">**DIREITOS DO \_ WMT**</span><span class="sxs-lookup"><span data-stu-id="355c8-128">**WMT\_RIGHTS**</span></span>](drm-wmt-rights.md)                                            | <span data-ttu-id="355c8-129">Define os direitos que podem ser especificados em uma licença drm.</span><span class="sxs-lookup"><span data-stu-id="355c8-129">Defines the rights that may be specified in a DRM license.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="355c8-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="355c8-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="355c8-131">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="355c8-131">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




