---
title: Atributos de estação multicast
description: Atributos de estação multicast
ms.assetid: 24b81ccb-4030-49a4-802c-5b45f7dd5950
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, estação multicast
- atributos de estação multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618ffa645055bf10a9247272d57c7e3f76853c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793894"
---
# <a name="multicast-station-attributes"></a><span data-ttu-id="79477-108">Atributos de estação multicast</span><span class="sxs-lookup"><span data-stu-id="79477-108">Multicast Station Attributes</span></span>

<span data-ttu-id="79477-109">Quando um arquivo é transmitido de uma estação de multicast, a estação pode impor alguns atributos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="79477-109">When a file is streaming from a multicast station, the station can impose some attributes on the file.</span></span> <span data-ttu-id="79477-110">Esses atributos, listados na tabela a seguir, não são realmente armazenados no arquivo e ficam disponíveis somente quando o arquivo é transmitido.</span><span class="sxs-lookup"><span data-stu-id="79477-110">These attributes, listed in the following table, are not actually stored in the file and are only available when the file is streaming.</span></span> <span data-ttu-id="79477-111">Eles contêm informações sobre a estação e normalmente seriam idênticos para todo o conteúdo da estação.</span><span class="sxs-lookup"><span data-stu-id="79477-111">They contain information about the station and would typically be identical for all content from the station.</span></span>



| <span data-ttu-id="79477-112">Atributo de estação multicast</span><span class="sxs-lookup"><span data-stu-id="79477-112">Multicast station attribute</span></span>                 | <span data-ttu-id="79477-113">Identificador global</span><span class="sxs-lookup"><span data-stu-id="79477-113">Global identifier</span></span>      | <span data-ttu-id="79477-114">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="79477-114">Data type</span></span>             |
|---------------------------------------------|------------------------|-----------------------|
| [<span data-ttu-id="79477-115">**\_Endereço NSC**</span><span class="sxs-lookup"><span data-stu-id="79477-115">**NSC\_Address**</span></span>](nsc-address.md)         | <span data-ttu-id="79477-116">g \_ wszWMNSCAddress</span><span class="sxs-lookup"><span data-stu-id="79477-116">g\_wszWMNSCAddress</span></span>     | <span data-ttu-id="79477-117">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="79477-117">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="79477-118">**Descrição de NSC \_**</span><span class="sxs-lookup"><span data-stu-id="79477-118">**NSC\_Description**</span></span>](nsc-description.md) | <span data-ttu-id="79477-119">g \_ wszWMNSCDescription</span><span class="sxs-lookup"><span data-stu-id="79477-119">g\_wszWMNSCDescription</span></span> | <span data-ttu-id="79477-120">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="79477-120">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="79477-121">**\_Email NSC**</span><span class="sxs-lookup"><span data-stu-id="79477-121">**NSC\_Email**</span></span>](nsc-email.md)             | <span data-ttu-id="79477-122">g \_ wszWMNSCEmail</span><span class="sxs-lookup"><span data-stu-id="79477-122">g\_wszWMNSCEmail</span></span>       | <span data-ttu-id="79477-123">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="79477-123">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="79477-124">**Nome de NSC \_**</span><span class="sxs-lookup"><span data-stu-id="79477-124">**NSC\_Name**</span></span>](nsc-name.md)               | <span data-ttu-id="79477-125">g \_ wszWMNSCName</span><span class="sxs-lookup"><span data-stu-id="79477-125">g\_wszWMNSCName</span></span>        | <span data-ttu-id="79477-126">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="79477-126">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="79477-127">**\_Telefone NSC**</span><span class="sxs-lookup"><span data-stu-id="79477-127">**NSC\_Phone**</span></span>](nsc-phone.md)             | <span data-ttu-id="79477-128">g \_ wszWMNSCPhone</span><span class="sxs-lookup"><span data-stu-id="79477-128">g\_wszWMNSCPhone</span></span>       | <span data-ttu-id="79477-129">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="79477-129">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="79477-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79477-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79477-131">**Atributos por tipo**</span><span class="sxs-lookup"><span data-stu-id="79477-131">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="79477-132">**Lista de Atributos**</span><span class="sxs-lookup"><span data-stu-id="79477-132">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




