---
title: Tipo complexo exmessagetype
description: Define os elementos que representam uma ação que mostra uma caixa de mensagem.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- tipo complexo de defaultmessagetype Agendador de Tarefas
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918741"
---
# <a name="showmessagetype-complex-type"></a><span data-ttu-id="07c46-104">Tipo complexo exmessagetype</span><span class="sxs-lookup"><span data-stu-id="07c46-104">showMessageType Complex Type</span></span>

<span data-ttu-id="07c46-105">Define os elementos que representam uma ação que mostra uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="07c46-105">Defines the elements that represent an action that shows a message box.</span></span>

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="07c46-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="07c46-106">Child elements</span></span>



| <span data-ttu-id="07c46-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="07c46-107">Element</span></span>                                                            | <span data-ttu-id="07c46-108">Type</span><span class="sxs-lookup"><span data-stu-id="07c46-108">Type</span></span>           | <span data-ttu-id="07c46-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="07c46-109">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="07c46-110">**Corpo**</span><span class="sxs-lookup"><span data-stu-id="07c46-110">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="07c46-111">não vazio</span><span class="sxs-lookup"><span data-stu-id="07c46-111">nonEmptyString</span></span> | <span data-ttu-id="07c46-112">Especifica o texto a ser exibido no corpo da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="07c46-112">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="07c46-113">**Título**</span><span class="sxs-lookup"><span data-stu-id="07c46-113">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="07c46-114">não vazio</span><span class="sxs-lookup"><span data-stu-id="07c46-114">nonEmptyString</span></span> | <span data-ttu-id="07c46-115">Especifica o título da caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="07c46-115">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="requirements"></a><span data-ttu-id="07c46-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c46-116">Requirements</span></span>



| <span data-ttu-id="07c46-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c46-117">Requirement</span></span> | <span data-ttu-id="07c46-118">Valor</span><span class="sxs-lookup"><span data-stu-id="07c46-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07c46-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07c46-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07c46-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07c46-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07c46-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07c46-121">Minimum supported server</span></span><br/> | <span data-ttu-id="07c46-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="07c46-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





