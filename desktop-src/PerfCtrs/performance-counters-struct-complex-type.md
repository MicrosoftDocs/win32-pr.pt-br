---
description: Define uma estrutura que contém um ou mais valores de contador.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Tipo complexo de struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756697"
---
# <a name="struct-complex-type"></a><span data-ttu-id="81167-103">Tipo complexo de struct</span><span class="sxs-lookup"><span data-stu-id="81167-103">struct Complex Type</span></span>

<span data-ttu-id="81167-104">Define uma estrutura que contém um ou mais valores de contador.</span><span class="sxs-lookup"><span data-stu-id="81167-104">Defines a structure that contains one or more counter values.</span></span>

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="81167-105">Atributos</span><span class="sxs-lookup"><span data-stu-id="81167-105">Attributes</span></span>



| <span data-ttu-id="81167-106">Nome</span><span class="sxs-lookup"><span data-stu-id="81167-106">Name</span></span> | <span data-ttu-id="81167-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="81167-107">Type</span></span>                                                                    | <span data-ttu-id="81167-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="81167-108">Description</span></span>                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81167-109">name</span><span class="sxs-lookup"><span data-stu-id="81167-109">name</span></span> | [<span data-ttu-id="81167-110">**homem: CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="81167-110">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="81167-111">O nome da estrutura.</span><span class="sxs-lookup"><span data-stu-id="81167-111">The name of the structure.</span></span><br/>                                                                                                            |
| <span data-ttu-id="81167-112">tipo</span><span class="sxs-lookup"><span data-stu-id="81167-112">type</span></span> | [<span data-ttu-id="81167-113">**homem: CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="81167-113">**man:CSymbolType**</span></span>](performance-counters-csymboltype-simple-type.md) | <span data-ttu-id="81167-114">Um nome simbólico que identifica a estrutura.</span><span class="sxs-lookup"><span data-stu-id="81167-114">A symbolic name that identifies the structure.</span></span> <span data-ttu-id="81167-115">A ferramenta [ctrpp](ctrpp.md) cria uma variável de struct com esse nome que você pode usar.</span><span class="sxs-lookup"><span data-stu-id="81167-115">The [CTRPP](ctrpp.md) tool creates a struct variable with this name that you can use.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="81167-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81167-116">Requirements</span></span>



| <span data-ttu-id="81167-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81167-117">Requirement</span></span> | <span data-ttu-id="81167-118">Valor</span><span class="sxs-lookup"><span data-stu-id="81167-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="81167-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81167-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81167-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81167-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="81167-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81167-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81167-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81167-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




