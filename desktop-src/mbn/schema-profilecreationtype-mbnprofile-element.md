---
description: Contém informações sobre o criador do perfil.
ms.assetid: a3adb323-d1de-4026-976e-a106007f4cc2
title: Elemento ProfileCreationType (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProfileCreationType
api_type:
- Schema
ms.openlocfilehash: 661306cf53b1ae4c7c9cd49a295afe5b84dabd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090581"
---
# <a name="profilecreationtype-mbnprofile-element"></a><span data-ttu-id="7b998-103">Elemento ProfileCreationType (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="7b998-103">ProfileCreationType (MBNProfile) Element</span></span>

<span data-ttu-id="7b998-104">O elemento **ProfileCreationType (MBNProfile)** contém informações sobre o criador do perfil.</span><span class="sxs-lookup"><span data-stu-id="7b998-104">The **ProfileCreationType (MBNProfile)** element contains information about the creator of the profile.</span></span>

<span data-ttu-id="7b998-105">Esse elemento pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b998-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="7b998-106">Valor</span><span class="sxs-lookup"><span data-stu-id="7b998-106">Value</span></span>                 | <span data-ttu-id="7b998-107">Significado</span><span class="sxs-lookup"><span data-stu-id="7b998-107">Meaning</span></span>                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b998-108">"Userprovisionado"</span><span class="sxs-lookup"><span data-stu-id="7b998-108">"UserProvisioned"</span></span>     | <span data-ttu-id="7b998-109">Esse perfil é criado por informações fornecidas pelo usuário do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b998-109">This profile is created by information provided by the user of device.</span></span>                                                     |
| <span data-ttu-id="7b998-110">"AdminProvisioned"</span><span class="sxs-lookup"><span data-stu-id="7b998-110">"AdminProvisioned"</span></span>    | <span data-ttu-id="7b998-111">Esse perfil é criado por administradores de ti e distribuído aos usuários.</span><span class="sxs-lookup"><span data-stu-id="7b998-111">This profile is created by IT administrators and distributed to users.</span></span>                                                     |
| <span data-ttu-id="7b998-112">"OperatorProvisioned"</span><span class="sxs-lookup"><span data-stu-id="7b998-112">"OperatorProvisioned"</span></span> | <span data-ttu-id="7b998-113">Esse perfil é criado por um operador de rede e distribuído aos usuários.</span><span class="sxs-lookup"><span data-stu-id="7b998-113">This profile is created by a network operator and distributed to users.</span></span>                                                    |
| <span data-ttu-id="7b998-114">"DeviceProvisioned"</span><span class="sxs-lookup"><span data-stu-id="7b998-114">"DeviceProvisioned"</span></span>   | <span data-ttu-id="7b998-115">Esse perfil é criado pelo serviço de banda larga móvel usando as informações armazenadas no contexto provisionado do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7b998-115">This profile is created by the Mobile Broadband service by using the information stored in the device provisioned context.</span></span> |



 

<span data-ttu-id="7b998-116">Esse é um elemento opcional.</span><span class="sxs-lookup"><span data-stu-id="7b998-116">This is an optional element.</span></span>

``` syntax
<xs:element name="ProfileCreationType">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="UserProvisioned"
             />
            <xs:enumeration
                value="AdminProvisioned"
             />
            <xs:enumeration
                value="OperatorProvisioned"
             />
            <xs:enumeration
                value="DeviceProvisioned"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="7b998-117">O elemento **ProfileCreationType** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7b998-117">The **ProfileCreationType** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b998-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b998-118">Requirements</span></span>



| <span data-ttu-id="7b998-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b998-119">Requirement</span></span> | <span data-ttu-id="7b998-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7b998-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="7b998-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b998-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7b998-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7b998-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="7b998-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b998-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7b998-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7b998-124">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="7b998-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b998-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7b998-126">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="7b998-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7b998-127">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="7b998-127">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="7b998-128">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="7b998-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7b998-129">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="7b998-129">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




