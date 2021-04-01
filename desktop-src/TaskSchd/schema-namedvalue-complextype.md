---
title: Tipo complexo nomeadovalue
description: Define um nome que está associado a um valor em um par de nome-valor.
ms.assetid: 5e3ce01a-9be6-4f12-be02-42065aba46cd
keywords:
- tipo complexo nomeadovalue Agendador de Tarefas
topic_type:
- apiref
api_name:
- namedValue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39d6990194350dcc032d42838f30bdd7339b0d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918745"
---
# <a name="namedvalue-complex-type"></a><span data-ttu-id="59631-104">Tipo complexo nomeadovalue</span><span class="sxs-lookup"><span data-stu-id="59631-104">namedValue Complex Type</span></span>

<span data-ttu-id="59631-105">Define um nome que está associado a um valor em um par de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="59631-105">Defines a name that is associated with a value in a name-value pair.</span></span>

``` syntax
<xs:complexType name="namedValue">
    <xs:simpleContent>
        <xs:extension
            base="nonEmptyString"
        >
            <xs:attribute name="name"
                type="nonEmptyString"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="59631-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="59631-106">Attributes</span></span>



| <span data-ttu-id="59631-107">Nome</span><span class="sxs-lookup"><span data-stu-id="59631-107">Name</span></span> | <span data-ttu-id="59631-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="59631-108">Type</span></span>                                                                    | <span data-ttu-id="59631-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="59631-109">Description</span></span>                                                                          |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="59631-110">name</span><span class="sxs-lookup"><span data-stu-id="59631-110">name</span></span> | [<span data-ttu-id="59631-111">**não vazio**</span><span class="sxs-lookup"><span data-stu-id="59631-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="59631-112">Especifica o nome que está associado a um valor em um par de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="59631-112">Specifies the name that is associated with a value in a name-value pair.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="59631-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59631-113">Requirements</span></span>



| <span data-ttu-id="59631-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="59631-114">Requirement</span></span> | <span data-ttu-id="59631-115">Valor</span><span class="sxs-lookup"><span data-stu-id="59631-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59631-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59631-116">Minimum supported client</span></span><br/> | <span data-ttu-id="59631-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59631-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59631-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59631-118">Minimum supported server</span></span><br/> | <span data-ttu-id="59631-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59631-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





