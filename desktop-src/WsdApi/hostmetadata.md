---
description: Define os metadados de hospedagem para o dispositivo a ser implementado. Este elemento é usado apenas para implementações de dispositivo (hosts).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994793"
---
# <a name="hostmetadata-element"></a><span data-ttu-id="5e475-104">elemento hostMetadata</span><span class="sxs-lookup"><span data-stu-id="5e475-104">hostMetadata element</span></span>

<span data-ttu-id="5e475-105">Define os metadados de hospedagem para o dispositivo a ser implementado.</span><span class="sxs-lookup"><span data-stu-id="5e475-105">Defines the hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="5e475-106">Este elemento é usado apenas para implementações de dispositivo (hosts).</span><span class="sxs-lookup"><span data-stu-id="5e475-106">This element is used for device implementations (hosts) only.</span></span>

## <a name="usage"></a><span data-ttu-id="5e475-107">Uso</span><span class="sxs-lookup"><span data-stu-id="5e475-107">Usage</span></span>

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a><span data-ttu-id="5e475-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e475-108">Attributes</span></span>

<span data-ttu-id="5e475-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="5e475-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5e475-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5e475-110">Child elements</span></span>



| <span data-ttu-id="5e475-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e475-111">Element</span></span>                             | <span data-ttu-id="5e475-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e475-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e475-113">**hospedeira**</span><span class="sxs-lookup"><span data-stu-id="5e475-113">**host**</span></span>](host.md)<br/>     | <span data-ttu-id="5e475-114">Define os elementos ServiceId e [**Types**](types.md) para o host de serviço.</span><span class="sxs-lookup"><span data-stu-id="5e475-114">Defines the ServiceID and [**Types**](types.md) elements for the service host.</span></span> <span data-ttu-id="5e475-115">Se não for fornecido explicitamente, o WSDAPI não fornecerá nenhum dado padrão em resposta a solicitações de metadados.</span><span class="sxs-lookup"><span data-stu-id="5e475-115">If not provided explicitly, WSDAPI will not supply any default data in response to metadata requests.</span></span><br/> <br/>                                                                                                                                          |
| [<span data-ttu-id="5e475-116">**hospedado**</span><span class="sxs-lookup"><span data-stu-id="5e475-116">**hosted**</span></span>](hosted.md)<br/> | <span data-ttu-id="5e475-117">Define os elementos [**ServiceId**](serviceid.md) e [**Types**](types.md) para os serviços fornecidos por esse host de serviço.</span><span class="sxs-lookup"><span data-stu-id="5e475-117">Defines the [**ServiceID**](serviceid.md) and [**Types**](types.md) elements for the services provided by this service host.</span></span> <span data-ttu-id="5e475-118">Cada serviço fornecido por esse host de serviço deve ter suas próprias informações de elemento [**hospedado**](hosted.md) para garantir que o serviço seja publicado corretamente em respostas a solicitações de metadados.</span><span class="sxs-lookup"><span data-stu-id="5e475-118">Each service provided by this service host should have its own [**hosted**](hosted.md) element information to ensure that the service is published properly in responses to metadata requests.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="5e475-119">Sequência de elementos filho</span><span class="sxs-lookup"><span data-stu-id="5e475-119">Child element sequence</span></span>

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a><span data-ttu-id="5e475-120">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5e475-120">Parent elements</span></span>



| <span data-ttu-id="5e475-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="5e475-121">Element</span></span>                                                         | <span data-ttu-id="5e475-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e475-122">Description</span></span>                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="5e475-123">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="5e475-123">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="5e475-124">Descreve o host e os metadados hospedados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e475-124">Describes the host and hosted metadata for the device.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5e475-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e475-125">Remarks</span></span>

<span data-ttu-id="5e475-126">Os metadados de hospedagem aparecem nesse elemento em um formato semelhante ao especificado no perfil do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e475-126">The hosting metadata appears in this element in a form similar to the one specified in the device profile.</span></span> <span data-ttu-id="5e475-127">**hostMetadata** é um pouco diferente do formato descrito no perfil do dispositivo no qual a única propriedade de referência à qual ele dá suporte é a ID do serviço.</span><span class="sxs-lookup"><span data-stu-id="5e475-127">**hostMetadata** is slightly different from the format described in the device profile in that the only reference property it supports is the service ID.</span></span>

<span data-ttu-id="5e475-128">O elemento [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) é usado subsequentemente para gerar uma constante C que contém essas informações.</span><span class="sxs-lookup"><span data-stu-id="5e475-128">The [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) element is used subsequently to generate a C constant containing this information.</span></span>

## <a name="element-information"></a><span data-ttu-id="5e475-129">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5e475-129">Element information</span></span>



| <span data-ttu-id="5e475-130">Label</span><span class="sxs-lookup"><span data-stu-id="5e475-130">Label</span></span> | <span data-ttu-id="5e475-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5e475-131">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="5e475-132">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e475-132">Minimum supported system</span></span><br/> | <span data-ttu-id="5e475-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5e475-133">Windows Vista</span></span> |
| <span data-ttu-id="5e475-134">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="5e475-134">Can be empty</span></span>                        | <span data-ttu-id="5e475-135">Não</span><span class="sxs-lookup"><span data-stu-id="5e475-135">No</span></span>            |



 

 




