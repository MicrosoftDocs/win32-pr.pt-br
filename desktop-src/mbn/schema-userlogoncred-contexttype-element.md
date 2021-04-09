---
description: Contém credenciais de logon para uma conexão.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Elemento UserLogonCred (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090578"
---
# <a name="userlogoncred-contexttype-element"></a><span data-ttu-id="6aaee-103">Elemento UserLogonCred (contextType)</span><span class="sxs-lookup"><span data-stu-id="6aaee-103">UserLogonCred (contextType) Element</span></span>

<span data-ttu-id="6aaee-104">O elemento **UserLogonCred (ContextType)** contém credenciais de logon para uma conexão.</span><span class="sxs-lookup"><span data-stu-id="6aaee-104">The **UserLogonCred (contextType)** element contains logon credentials for a connection.</span></span>

<span data-ttu-id="6aaee-105">Esse elemento pode ter os seguintes elementos filho.</span><span class="sxs-lookup"><span data-stu-id="6aaee-105">This element can have the following child elements.</span></span>

-   [<span data-ttu-id="6aaee-106">**Usu**</span><span class="sxs-lookup"><span data-stu-id="6aaee-106">**UserName**</span></span>](schema-username-userlogoncred-element.md)
-   [<span data-ttu-id="6aaee-107">**Senha**</span><span class="sxs-lookup"><span data-stu-id="6aaee-107">**Password**</span></span>](schema-password-userlogoncred-element.md)
-   [<span data-ttu-id="6aaee-108">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="6aaee-108">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md)

<span data-ttu-id="6aaee-109">Esse elemento pode ter um máximo de uma ocorrência.</span><span class="sxs-lookup"><span data-stu-id="6aaee-109">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="6aaee-110">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="6aaee-110">This element is optional.</span></span>

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="6aaee-111">O elemento **UserLogonCred** é definido pelo tipo complexo [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6aaee-111">The **UserLogonCred** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6aaee-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6aaee-112">Child elements</span></span>



| <span data-ttu-id="6aaee-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="6aaee-113">Element</span></span>                                                               | <span data-ttu-id="6aaee-114">Type</span><span class="sxs-lookup"><span data-stu-id="6aaee-114">Type</span></span>                                           | <span data-ttu-id="6aaee-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6aaee-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="6aaee-116">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="6aaee-116">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="6aaee-117">booleano</span><span class="sxs-lookup"><span data-stu-id="6aaee-117">boolean</span></span>                                        | <span data-ttu-id="6aaee-118">Como lidar com senhas ao atualizar perfis.</span><span class="sxs-lookup"><span data-stu-id="6aaee-118">How to handle passwords when upgrading profiles.</span></span><br/> |
| [<span data-ttu-id="6aaee-119">**Senha**</span><span class="sxs-lookup"><span data-stu-id="6aaee-119">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="6aaee-120">string</span><span class="sxs-lookup"><span data-stu-id="6aaee-120">string</span></span>                                         | <span data-ttu-id="6aaee-121">Senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="6aaee-121">User password.</span></span><br/>                                   |
| [<span data-ttu-id="6aaee-122">**Usu**</span><span class="sxs-lookup"><span data-stu-id="6aaee-122">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="6aaee-123">**nometype**</span><span class="sxs-lookup"><span data-stu-id="6aaee-123">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="6aaee-124">Nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="6aaee-124">User name.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="6aaee-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6aaee-125">Requirements</span></span>



| <span data-ttu-id="6aaee-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aaee-126">Requirement</span></span> | <span data-ttu-id="6aaee-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6aaee-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="6aaee-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6aaee-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6aaee-129">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6aaee-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="6aaee-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6aaee-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6aaee-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6aaee-131">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="6aaee-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6aaee-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="6aaee-133">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="6aaee-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6aaee-134">**contextType**</span><span class="sxs-lookup"><span data-stu-id="6aaee-134">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="6aaee-135">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="6aaee-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6aaee-136">**Contexto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="6aaee-136">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




