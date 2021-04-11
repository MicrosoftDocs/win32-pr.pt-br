---
title: Tipo complexo TemplateItemType
description: Um modelo que define os dados a serem incluídos com um evento. | Tipo complexo TemplateItemType
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- Log de eventos do tipo complexo TemplateItemType
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172758"
---
# <a name="templateitemtype-complex-type"></a><span data-ttu-id="ece50-105">Tipo complexo TemplateItemType</span><span class="sxs-lookup"><span data-stu-id="ece50-105">TemplateItemType Complex Type</span></span>

<span data-ttu-id="ece50-106">Um modelo que define os dados a serem incluídos com um evento.</span><span class="sxs-lookup"><span data-stu-id="ece50-106">A template that defines the data to include with an event.</span></span>

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ece50-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ece50-107">Child elements</span></span>



| <span data-ttu-id="ece50-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="ece50-108">Element</span></span>                                                                   | <span data-ttu-id="ece50-109">Type</span><span class="sxs-lookup"><span data-stu-id="ece50-109">Type</span></span>                                                                                 | <span data-ttu-id="ece50-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ece50-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ece50-111">**binary**</span><span class="sxs-lookup"><span data-stu-id="ece50-111">**binary**</span></span>](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | <span data-ttu-id="ece50-112">Reservado apenas para uso interno.</span><span class="sxs-lookup"><span data-stu-id="ece50-112">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="ece50-113">**dado**</span><span class="sxs-lookup"><span data-stu-id="ece50-113">**data**</span></span>](eventmanifestschema-data-templateitemtype-element.md)         | [<span data-ttu-id="ece50-114">**Datadefinitiontype**</span><span class="sxs-lookup"><span data-stu-id="ece50-114">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md)     | <span data-ttu-id="ece50-115">Define um item de dados que você deseja incluir com o evento.</span><span class="sxs-lookup"><span data-stu-id="ece50-115">Defines a data item that you want to include with the event.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="ece50-116">**struct**</span><span class="sxs-lookup"><span data-stu-id="ece50-116">**struct**</span></span>](eventmanifestschema-struct-templateitemtype-element.md)     | [<span data-ttu-id="ece50-117">**StructDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="ece50-117">**StructDefinitionType**</span></span>](eventmanifestschema-structdefinitiontype-complextype.md) | <span data-ttu-id="ece50-118">Define uma estrutura que inclui um ou mais itens de dados que você deseja incluir com o evento.</span><span class="sxs-lookup"><span data-stu-id="ece50-118">Defines a structure that includes one or more data items that you want to include with the event.</span></span> <span data-ttu-id="ece50-119">Os provedores gravam a estrutura como um blob e não como membros individuais da estrutura.</span><span class="sxs-lookup"><span data-stu-id="ece50-119">Providers write the structure as a blob and not as individual members of the structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ece50-120">**UserData**</span><span class="sxs-lookup"><span data-stu-id="ece50-120">**UserData**</span></span>](eventmanifestschema-userdata-templateitemtype-element.md) | [<span data-ttu-id="ece50-121">**XmlType**</span><span class="sxs-lookup"><span data-stu-id="ece50-121">**XmlType**</span></span>](eventmanifestschema-xmltype-complextype.md)                           | <span data-ttu-id="ece50-122">Um fragmento XML que é usado para renderizar os dados do evento.</span><span class="sxs-lookup"><span data-stu-id="ece50-122">An XML fragment that is used to render the event data.</span></span> <span data-ttu-id="ece50-123">Se você não incluir o fragmento, os dados do evento serão renderizados na ordem em que os itens de dados são definidos no modelo.</span><span class="sxs-lookup"><span data-stu-id="ece50-123">If you do not include the fragment, the event data is rendered in the order that the data items are defined in the template.</span></span> <span data-ttu-id="ece50-124">O conteúdo desse elemento é qualquer fragmento XML válido.</span><span class="sxs-lookup"><span data-stu-id="ece50-124">The contents of this element is any valid XML fragment.</span></span> <span data-ttu-id="ece50-125">O fragmento deve conter apenas um nó de nível superior e o nó de nível superior deve especificar seu próprio namespace.</span><span class="sxs-lookup"><span data-stu-id="ece50-125">The fragment must contain only one top-level node and the top-level node must specify its own namespace.</span></span> <br/> <span data-ttu-id="ece50-126">Para fazer referência a um item de dados no fragmento, defina o corpo do texto para um nó no fragmento como%*n*, em que *n* é o índice baseado em um dos itens de dados de nível superior na lista de itens de dados (você não pode fazer referência a membros de uma estrutura).</span><span class="sxs-lookup"><span data-stu-id="ece50-126">To reference a data item in the fragment, set the text body for a node in the fragment to %*n*, where *n* is the one-based index of the top-level data items in the list of data items (you cannot reference members of a structure).</span></span> <span data-ttu-id="ece50-127">O valor de índice especificado não deve ser maior que o número de itens de dados de nível superior no modelo.</span><span class="sxs-lookup"><span data-stu-id="ece50-127">The index value that you specify must not be greater than the number of top-level data items in the template.</span></span><br/> <span data-ttu-id="ece50-128">Esse elemento segue todos os elementos de **dados** e **struct** .</span><span class="sxs-lookup"><span data-stu-id="ece50-128">This element follows all **data** and **struct** elements.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="ece50-129">Atributos</span><span class="sxs-lookup"><span data-stu-id="ece50-129">Attributes</span></span>



| <span data-ttu-id="ece50-130">Nome</span><span class="sxs-lookup"><span data-stu-id="ece50-130">Name</span></span> | <span data-ttu-id="ece50-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ece50-131">Type</span></span>   | <span data-ttu-id="ece50-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="ece50-132">Description</span></span>                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece50-133">name</span><span class="sxs-lookup"><span data-stu-id="ece50-133">name</span></span> | <span data-ttu-id="ece50-134">string</span><span class="sxs-lookup"><span data-stu-id="ece50-134">string</span></span> | <span data-ttu-id="ece50-135">Reservado apenas para uso interno.</span><span class="sxs-lookup"><span data-stu-id="ece50-135">Reserved for internal use only.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="ece50-136">name</span><span class="sxs-lookup"><span data-stu-id="ece50-136">name</span></span> | <span data-ttu-id="ece50-137">string</span><span class="sxs-lookup"><span data-stu-id="ece50-137">string</span></span> | <span data-ttu-id="ece50-138">O nome do modelo.</span><span class="sxs-lookup"><span data-stu-id="ece50-138">The name of the template.</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="ece50-139">tid</span><span class="sxs-lookup"><span data-stu-id="ece50-139">tid</span></span>  | <span data-ttu-id="ece50-140">token</span><span class="sxs-lookup"><span data-stu-id="ece50-140">token</span></span>  | <span data-ttu-id="ece50-141">Um identificador que identifica exclusivamente o modelo dentro da lista de modelos que o provedor define.</span><span class="sxs-lookup"><span data-stu-id="ece50-141">An identifier that uniquely identifies the template within the list of templates that the provider defines.</span></span> <span data-ttu-id="ece50-142">Use esse nome para fazer referência ao modelo quando você definir sua definição de evento.</span><span class="sxs-lookup"><span data-stu-id="ece50-142">Use this name to reference the template when you define your event definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ece50-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="ece50-143">Remarks</span></span>

<span data-ttu-id="ece50-144">A definição do modelo deve ter pelo menos um elemento filho data ou struct.</span><span class="sxs-lookup"><span data-stu-id="ece50-144">The template definition must have at least one data or struct child element.</span></span> <span data-ttu-id="ece50-145">O provedor deve gravar os dados do evento na ordem dos itens de dados definidos no modelo.</span><span class="sxs-lookup"><span data-stu-id="ece50-145">The provider must write the event data in the order of the data items defined in the template.</span></span>

<span data-ttu-id="ece50-146">O tamanho de todos os itens de dados no modelo deve ser inferior a 64 KB.</span><span class="sxs-lookup"><span data-stu-id="ece50-146">The size of all the data items in the template must be less than 64 KB.</span></span>

## <a name="examples"></a><span data-ttu-id="ece50-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ece50-147">Examples</span></span>

<span data-ttu-id="ece50-148">O exemplo a seguir mostra como criar uma definição de modelo.</span><span class="sxs-lookup"><span data-stu-id="ece50-148">The following example shows how to create a template definition.</span></span>


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a><span data-ttu-id="ece50-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ece50-149">Requirements</span></span>



| <span data-ttu-id="ece50-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="ece50-150">Requirement</span></span> | <span data-ttu-id="ece50-151">Valor</span><span class="sxs-lookup"><span data-stu-id="ece50-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ece50-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece50-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ece50-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ece50-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ece50-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ece50-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ece50-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ece50-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





