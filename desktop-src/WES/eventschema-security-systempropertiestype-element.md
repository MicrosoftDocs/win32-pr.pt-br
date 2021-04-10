---
title: Elemento Security (SystemPropertiesType)
description: Identifica o usuário que registrou o evento.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Elemento de segurança EventLog
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086261"
---
# <a name="security-systempropertiestype-element"></a><span data-ttu-id="387e3-104">Elemento Security (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="387e3-104">Security (SystemPropertiesType) Element</span></span>

<span data-ttu-id="387e3-105">Identifica o usuário que registrou o evento.</span><span class="sxs-lookup"><span data-stu-id="387e3-105">Identifies the user that logged the event.</span></span>

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="387e3-106">O elemento **Security** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="387e3-106">The **Security** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="387e3-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="387e3-107">Attributes</span></span>



| <span data-ttu-id="387e3-108">Nome</span><span class="sxs-lookup"><span data-stu-id="387e3-108">Name</span></span>   | <span data-ttu-id="387e3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="387e3-109">Type</span></span>   | <span data-ttu-id="387e3-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="387e3-110">Description</span></span>                                                          |
|--------|--------|----------------------------------------------------------------------|
| <span data-ttu-id="387e3-111">UserID</span><span class="sxs-lookup"><span data-stu-id="387e3-111">UserID</span></span> | <span data-ttu-id="387e3-112">string</span><span class="sxs-lookup"><span data-stu-id="387e3-112">string</span></span> | <span data-ttu-id="387e3-113">O SID (identificador de segurança) do usuário no formulário de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="387e3-113">The security identifier (SID) of the user in string form.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="387e3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="387e3-114">Requirements</span></span>



| <span data-ttu-id="387e3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="387e3-115">Requirement</span></span> | <span data-ttu-id="387e3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="387e3-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="387e3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="387e3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="387e3-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="387e3-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="387e3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="387e3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="387e3-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="387e3-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="387e3-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="387e3-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="387e3-122">**Elemento pai**</span><span class="sxs-lookup"><span data-stu-id="387e3-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="387e3-123">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="387e3-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





