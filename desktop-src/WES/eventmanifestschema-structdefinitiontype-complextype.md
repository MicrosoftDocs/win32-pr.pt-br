---
title: Tipo complexo StructDefinitionType
description: Define uma estrutura que inclui um ou mais itens de dados que você deseja incluir com o evento. | Tipo complexo StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- Log de eventos do tipo complexo StructDefinitionType
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105813207"
---
# <a name="structdefinitiontype-complex-type"></a><span data-ttu-id="92786-105">Tipo complexo StructDefinitionType</span><span class="sxs-lookup"><span data-stu-id="92786-105">StructDefinitionType Complex Type</span></span>

<span data-ttu-id="92786-106">Define uma estrutura que inclui um ou mais itens de dados que você deseja incluir com o evento.</span><span class="sxs-lookup"><span data-stu-id="92786-106">Defines a structure that includes one or more data items that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="92786-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="92786-107">Child elements</span></span>



| <span data-ttu-id="92786-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="92786-108">Element</span></span>                                                               | <span data-ttu-id="92786-109">Type</span><span class="sxs-lookup"><span data-stu-id="92786-109">Type</span></span>                                                                             | <span data-ttu-id="92786-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="92786-110">Description</span></span>                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="92786-111">**dado**</span><span class="sxs-lookup"><span data-stu-id="92786-111">**data**</span></span>](eventmanifestschema-data-structdefinitiontype-element.md) | [<span data-ttu-id="92786-112">**Datadefinitiontype**</span><span class="sxs-lookup"><span data-stu-id="92786-112">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md) | <span data-ttu-id="92786-113">Define um item de dados que você deseja incluir na estrutura.</span><span class="sxs-lookup"><span data-stu-id="92786-113">Defines a data item that you want to include in the structure.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="92786-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="92786-114">Attributes</span></span>



| <span data-ttu-id="92786-115">Nome</span><span class="sxs-lookup"><span data-stu-id="92786-115">Name</span></span>   | <span data-ttu-id="92786-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="92786-116">Type</span></span>                                                            | <span data-ttu-id="92786-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="92786-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92786-118">count</span><span class="sxs-lookup"><span data-stu-id="92786-118">count</span></span>  | [<span data-ttu-id="92786-119">**Número de contagem**</span><span class="sxs-lookup"><span data-stu-id="92786-119">**CountType**</span></span>](eventmanifestschema-counttype-simpletype.md)   | <span data-ttu-id="92786-120">O número de elementos em uma matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="92786-120">The number of elements in an array of structures.</span></span> <span data-ttu-id="92786-121">Esse atributo indica que a estrutura está definindo uma matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="92786-121">This attribute indicates that the structure is defining an array of structures.</span></span> <span data-ttu-id="92786-122">Você pode especificar a contagem real ou o nome de um item de dados fora da estrutura que contém a contagem.</span><span class="sxs-lookup"><span data-stu-id="92786-122">You can specify the actual count or the name of a data item outside of the structure that contains the count.</span></span> <br/>                               |
| <span data-ttu-id="92786-123">comprimento</span><span class="sxs-lookup"><span data-stu-id="92786-123">length</span></span> | [<span data-ttu-id="92786-124">**Comprimentotype**</span><span class="sxs-lookup"><span data-stu-id="92786-124">**LengthType**</span></span>](eventmanifestschema-lengthtype-simpletype.md) | <span data-ttu-id="92786-125">Não disponível.</span><span class="sxs-lookup"><span data-stu-id="92786-125">Not available.</span></span><br/> <span data-ttu-id="92786-126">**Windows Server 2008 e Windows Vista:** O comprimento dessa estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="92786-126">**Windows Server 2008 and Windows Vista:** The length of this structure, in bytes.</span></span> <span data-ttu-id="92786-127">Não disponível a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92786-127">Not available starting with Windows 7.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="92786-128">name</span><span class="sxs-lookup"><span data-stu-id="92786-128">name</span></span>   | <span data-ttu-id="92786-129">string</span><span class="sxs-lookup"><span data-stu-id="92786-129">string</span></span>                                                          | <span data-ttu-id="92786-130">O nome para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="92786-130">The name to the structure.</span></span> <span data-ttu-id="92786-131">Você pode usar o nome para fazer referência ao item de dados no fragmento XML se especificar uma seção [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) em seu modelo.</span><span class="sxs-lookup"><span data-stu-id="92786-131">You can use the name to reference the data item in your XML fragment if you specify a [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) section in your template.</span></span><br/> <span data-ttu-id="92786-132">**Windows Vista:** Esse atributo é opcional.</span><span class="sxs-lookup"><span data-stu-id="92786-132">**Windows Vista:** This attribute is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="92786-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="92786-133">Remarks</span></span>

<span data-ttu-id="92786-134">Os provedores gravam a estrutura como um blob e não como membros individuais da estrutura.</span><span class="sxs-lookup"><span data-stu-id="92786-134">Providers write the structure as a blob and not as individual members of the structure.</span></span> <span data-ttu-id="92786-135">Se a estrutura C que você está escrevendo contiver ponteiros (por exemplo, um ponteiro do tipo LPWSTR), os dados do evento conterão o valor do ponteiro, não os dados desreferenciados.</span><span class="sxs-lookup"><span data-stu-id="92786-135">If the C structure that you are writing contains pointers (for example, a pointer of type LPWSTR), the event data will contain the pointer value, not the dereferenced data.</span></span>

<span data-ttu-id="92786-136">Você não deve usar estruturas, mas, em vez disso, deve definir itens de dados para cada membro e gravá-los separadamente.</span><span class="sxs-lookup"><span data-stu-id="92786-136">You should not use structures but instead should define data items for each member and write them separately.</span></span> <span data-ttu-id="92786-137">Se você decidir usar estrutura, a estrutura deverá conter apenas tipos integrais e você deverá garantir que os membros da estrutura fiquem alinhados a um limite de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="92786-137">If you decide to use structure, the structure should contain only integral types and you must ensure that the members of the structure align to an 8-byte boundary.</span></span> <span data-ttu-id="92786-138">Se você não fizer isso, provavelmente receberá erros de alinhamento ao tentar acessar os dados.</span><span class="sxs-lookup"><span data-stu-id="92786-138">If you do not, you will likely receive alignment errors when you try to access the data.</span></span> <span data-ttu-id="92786-139">Considere usar a \# diretiva pragma Pack () para forçar o alinhamento em um limite de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="92786-139">Consider using the \#pragma pack() directive to force alignment on an 8-byte boundary.</span></span>

## <a name="requirements"></a><span data-ttu-id="92786-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92786-140">Requirements</span></span>



| <span data-ttu-id="92786-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="92786-141">Requirement</span></span> | <span data-ttu-id="92786-142">Valor</span><span class="sxs-lookup"><span data-stu-id="92786-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92786-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92786-143">Minimum supported client</span></span><br/> | <span data-ttu-id="92786-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92786-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92786-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92786-145">Minimum supported server</span></span><br/> | <span data-ttu-id="92786-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92786-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





