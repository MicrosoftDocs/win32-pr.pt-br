---
title: Tipo complexo OpcodeListType
description: Define uma lista de opcodes que são usados para identificar as operações de um componente do aplicativo.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- Log de eventos do tipo complexo OpcodeListType
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455083"
---
# <a name="opcodelisttype-complex-type"></a><span data-ttu-id="46b7c-104">Tipo complexo OpcodeListType</span><span class="sxs-lookup"><span data-stu-id="46b7c-104">OpcodeListType Complex Type</span></span>

<span data-ttu-id="46b7c-105">Define uma lista de opcodes que são usados para identificar as operações de um componente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46b7c-105">Defines a list of opcodes that are used to identify the operations of a component of the application.</span></span>

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="46b7c-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="46b7c-106">Child elements</span></span>



| <span data-ttu-id="46b7c-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="46b7c-107">Element</span></span>                                                             | <span data-ttu-id="46b7c-108">Type</span><span class="sxs-lookup"><span data-stu-id="46b7c-108">Type</span></span>                                                             | <span data-ttu-id="46b7c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="46b7c-109">Description</span></span>                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="46b7c-110">**opcode**</span><span class="sxs-lookup"><span data-stu-id="46b7c-110">**opcode**</span></span>](eventmanifestschema-opcode-opcodelisttype-element.md) | [<span data-ttu-id="46b7c-111">**OpCodeType**</span><span class="sxs-lookup"><span data-stu-id="46b7c-111">**OpcodeType**</span></span>](eventmanifestschema-opcodetype-complextype.md) | <span data-ttu-id="46b7c-112">Define uma operação dentro de um componente do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="46b7c-112">Defines an operation within a component of the application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="46b7c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46b7c-113">Requirements</span></span>



| <span data-ttu-id="46b7c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b7c-114">Requirement</span></span> | <span data-ttu-id="46b7c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="46b7c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46b7c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46b7c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46b7c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46b7c-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46b7c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46b7c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46b7c-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46b7c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





