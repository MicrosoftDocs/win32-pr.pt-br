---
description: Especifica o arquivo inteiro por trás do objeto. Também é uma maneira de se referir a qualquer tipo de recurso, incluindo aqueles não cobertos por outros tipos de recursos de dispositivos portáteis do Windows, como um tipo de objeto personalizado.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506140"
---
# <a name="wpd_resource_default"></a><span data-ttu-id="29ecb-104">\_padrão de recursos WPD \_</span><span class="sxs-lookup"><span data-stu-id="29ecb-104">WPD\_RESOURCE\_DEFAULT</span></span>

<span data-ttu-id="29ecb-105">Especifica o arquivo inteiro por trás do objeto.</span><span class="sxs-lookup"><span data-stu-id="29ecb-105">Specifies the whole file behind the object.</span></span> <span data-ttu-id="29ecb-106">Também é uma maneira de se referir a qualquer tipo de recurso, incluindo aqueles não cobertos por outros tipos de recursos de dispositivos portáteis do Windows, como um tipo de objeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="29ecb-106">It is also a way of referring to any resource type, including those not covered by other Windows Portable Devices resource types, such as a custom object type.</span></span>

<span data-ttu-id="29ecb-107">Todos os recursos inseridos no recurso especificado serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="29ecb-107">Any resources embedded within the specified resource will be included.</span></span> <span data-ttu-id="29ecb-108">Por exemplo, o recurso padrão de uma pasta raiz de contatos pode incluir todos os contatos aninhados.</span><span class="sxs-lookup"><span data-stu-id="29ecb-108">For example, the default resource of a root folder of contacts may include all the nested contacts.</span></span> <span data-ttu-id="29ecb-109">No entanto, todos os recursos filho que são simplesmente *vinculados* por metadados ou referências não são incluídos.</span><span class="sxs-lookup"><span data-stu-id="29ecb-109">However, any child resources that are merely *linked* by metadata or references are not included.</span></span> <span data-ttu-id="29ecb-110">Um exemplo disso seria uma lista de reprodução, que só pode ser vinculada a arquivos de áudio por meio de referências de metadados ou referências de caminho textual no arquivo.</span><span class="sxs-lookup"><span data-stu-id="29ecb-110">An example of this would be a playlist, which might only link to audio files through metadata references or textual path references in the file.</span></span>

<span data-ttu-id="29ecb-111">O único valor *pid* permitido para este **PROPERTYKEY** é zero.</span><span class="sxs-lookup"><span data-stu-id="29ecb-111">The only allowed *pid* value for this **PROPERTYKEY** is zero.</span></span>

<span data-ttu-id="29ecb-112">Esse tipo de recurso deve dar suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="29ecb-112">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="29ecb-113">Nome do atributo</span><span class="sxs-lookup"><span data-stu-id="29ecb-113">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="29ecb-114">Obrigatório ou opcional</span><span class="sxs-lookup"><span data-stu-id="29ecb-114">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="29ecb-115">\_ \_ Tamanho total do atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="29ecb-115">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="29ecb-116">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="29ecb-116">Required.</span></span>                                              |
| [<span data-ttu-id="29ecb-117">o \_ atributo de recurso WPD \_ \_ pode \_ ler</span><span class="sxs-lookup"><span data-stu-id="29ecb-117">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="29ecb-118">Necessário se os clientes puderem ler este recurso.</span><span class="sxs-lookup"><span data-stu-id="29ecb-118">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="29ecb-119">o \_ atributo de recurso WPD \_ \_ pode \_ gravar</span><span class="sxs-lookup"><span data-stu-id="29ecb-119">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="29ecb-120">Necessário se os clientes puderem gravar nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="29ecb-120">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="29ecb-121">o \_ atributo de recurso WPD \_ \_ pode \_ excluir</span><span class="sxs-lookup"><span data-stu-id="29ecb-121">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="29ecb-122">Necessário se os clientes puderem excluir esse recurso.</span><span class="sxs-lookup"><span data-stu-id="29ecb-122">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="29ecb-123">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_</span><span class="sxs-lookup"><span data-stu-id="29ecb-123">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="29ecb-124">Necessário se os clientes tiverem acesso de leitura ao recurso.</span><span class="sxs-lookup"><span data-stu-id="29ecb-124">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="29ecb-125">\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_</span><span class="sxs-lookup"><span data-stu-id="29ecb-125">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="29ecb-126">Necessário se os clientes tiverem acesso de gravação ao recurso.</span><span class="sxs-lookup"><span data-stu-id="29ecb-126">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="29ecb-127">\_formato de \_ atributo de recurso WPD \_</span><span class="sxs-lookup"><span data-stu-id="29ecb-127">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="29ecb-128">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="29ecb-128">Required.</span></span>                                              |
| [<span data-ttu-id="29ecb-129">\_chave de \_ recurso de atributo de recurso WPD \_ \_</span><span class="sxs-lookup"><span data-stu-id="29ecb-129">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="29ecb-130">Recomendável.</span><span class="sxs-lookup"><span data-stu-id="29ecb-130">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="29ecb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="29ecb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ecb-132">**Requisitos para recursos**</span><span class="sxs-lookup"><span data-stu-id="29ecb-132">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



