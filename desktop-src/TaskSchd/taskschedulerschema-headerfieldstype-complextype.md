---
title: Tipo complexo headerFieldsType
description: Define os elementos que especificam os campos para um cabeçalho de email.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- Agendador de Tarefas tipo complexo headerFieldsType
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454895"
---
# <a name="headerfieldstype-complex-type"></a><span data-ttu-id="1725b-104">Tipo complexo headerFieldsType</span><span class="sxs-lookup"><span data-stu-id="1725b-104">headerFieldsType Complex Type</span></span>

<span data-ttu-id="1725b-105">Define os elementos que especificam os campos para um cabeçalho de email.</span><span class="sxs-lookup"><span data-stu-id="1725b-105">Defines the elements that specify the fields for an email header.</span></span>

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="1725b-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1725b-106">Child elements</span></span>



| <span data-ttu-id="1725b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1725b-107">Element</span></span>                                                                         | <span data-ttu-id="1725b-108">Type</span><span class="sxs-lookup"><span data-stu-id="1725b-108">Type</span></span>                                                                       | <span data-ttu-id="1725b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1725b-109">Description</span></span>                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="1725b-110">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="1725b-110">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="1725b-111">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="1725b-111">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="1725b-112">Especifica um campo em um cabeçalho de email.</span><span class="sxs-lookup"><span data-stu-id="1725b-112">Specifies a field in an email header.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="1725b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1725b-113">Requirements</span></span>



| <span data-ttu-id="1725b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1725b-114">Requirement</span></span> | <span data-ttu-id="1725b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1725b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1725b-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1725b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1725b-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1725b-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1725b-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1725b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1725b-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1725b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





