---
description: Define um atributo de um contador que especifica como os dados do contador são exibidos em um aplicativo de consumidor.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: Tipo complexo de atributo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753240"
---
# <a name="counterattribute-complex-type"></a><span data-ttu-id="1849c-103">Tipo complexo de atributo</span><span class="sxs-lookup"><span data-stu-id="1849c-103">counterAttribute Complex Type</span></span>

<span data-ttu-id="1849c-104">Define um atributo de um contador que especifica como os dados do contador são exibidos em um aplicativo de consumidor.</span><span class="sxs-lookup"><span data-stu-id="1849c-104">Defines an attribute of a counter that specifies how the counter data is displayed in a consumer application.</span></span>

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="1849c-105">Atributos</span><span class="sxs-lookup"><span data-stu-id="1849c-105">Attributes</span></span>



| <span data-ttu-id="1849c-106">Nome</span><span class="sxs-lookup"><span data-stu-id="1849c-106">Name</span></span> | <span data-ttu-id="1849c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1849c-107">Type</span></span> | <span data-ttu-id="1849c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1849c-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1849c-109">name</span><span class="sxs-lookup"><span data-stu-id="1849c-109">name</span></span> |      | <span data-ttu-id="1849c-110">O nome do atributo de exibição a ser aplicado.</span><span class="sxs-lookup"><span data-stu-id="1849c-110">The name of the display attribute to apply.</span></span> <span data-ttu-id="1849c-111">Você pode especificar um dos seguintes nomes:</span><span class="sxs-lookup"><span data-stu-id="1849c-111">You can specify one of the following names:</span></span><br/> <dl> <span data-ttu-id="1849c-112"><dt><span id="reference"></span><span id="REFERENCE"></span>referência</dt></span><span class="sxs-lookup"><span data-stu-id="1849c-112"><dt><span id="reference"></span><span id="REFERENCE"></span>reference</dt></span></span> <dd> <span data-ttu-id="1849c-113">Recupere o valor do contador por referência, em oposição ao valor.</span><span class="sxs-lookup"><span data-stu-id="1849c-113">Retrieve the value of the counter by reference as opposed to by value.</span></span><br/> </dd> <span data-ttu-id="1849c-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>NoDisplay</dt></span><span class="sxs-lookup"><span data-stu-id="1849c-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>noDisplay</dt></span></span> <dd> <span data-ttu-id="1849c-115">Não exiba o valor do contador.</span><span class="sxs-lookup"><span data-stu-id="1849c-115">Do not display the counter value.</span></span> <span data-ttu-id="1849c-116">Normalmente, você usará esse atributo se os dados do contador forem usados como entrada para calcular o valor de outro contador.</span><span class="sxs-lookup"><span data-stu-id="1849c-116">Typically, you use this attribute if the counter's data is used as input for calculating another counter's value.</span></span> <br/> </dd> <span data-ttu-id="1849c-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span><span class="sxs-lookup"><span data-stu-id="1849c-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span></span> <dd> <span data-ttu-id="1849c-118">Aplicativos de monitoramento ou de consumidor não devem usar separadores de dígitos ao exibir valores de contadores.</span><span class="sxs-lookup"><span data-stu-id="1849c-118">Consumer or monitoring applications should not use digit separators when displaying counter values.</span></span> <br/> </dd> <span data-ttu-id="1849c-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span><span class="sxs-lookup"><span data-stu-id="1849c-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span></span> <dd> <span data-ttu-id="1849c-120">Os aplicativos de monitoramento ou consumidor devem exibir o valor do contador como um hexadecimal, em vez do valor inteiro padrão.</span><span class="sxs-lookup"><span data-stu-id="1849c-120">Consumer or monitoring applications should display the counter value as a hexadecimal, instead of the default integer value.</span></span><br/> </dd> <span data-ttu-id="1849c-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span><span class="sxs-lookup"><span data-stu-id="1849c-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span></span> <dd> <span data-ttu-id="1849c-122">Os aplicativos de monitoramento ou consumidor devem exibir o valor do contador como um número real, em vez do valor inteiro padrão.</span><span class="sxs-lookup"><span data-stu-id="1849c-122">Consumer or monitoring applications should display the counter value as a real number, instead of the default integer value.</span></span> <br/> </dd> </dl> |



## <a name="requirements"></a><span data-ttu-id="1849c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1849c-123">Requirements</span></span>



| <span data-ttu-id="1849c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1849c-124">Requirement</span></span> | <span data-ttu-id="1849c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1849c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1849c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1849c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1849c-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1849c-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1849c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1849c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1849c-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1849c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




