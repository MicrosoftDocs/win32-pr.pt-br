---
description: Contém configurações do módulo de mídia específica (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Elemento MSM (LANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170412"
---
# <a name="msm-lanprofile-element"></a><span data-ttu-id="7ce7e-103">Elemento MSM (LANProfile)</span><span class="sxs-lookup"><span data-stu-id="7ce7e-103">MSM (LANProfile) Element</span></span>

<span data-ttu-id="7ce7e-104">O elemento MSM (LANProfile) contém configurações do módulo de mídia específica (MSM).</span><span class="sxs-lookup"><span data-stu-id="7ce7e-104">The MSM (LANProfile) element contains media-specific module (MSM) settings.</span></span>

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="security">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OneXEnforced"
                            type="boolean"
                         />
                        <xs:element name="OneXEnabled"
                            type="boolean"
                         />
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="7ce7e-105">O elemento **msm** é definido pelo elemento [**LANProfile**](lan-profileschema-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7ce7e-105">The **MSM** element is defined by the [**LANProfile**](lan-profileschema-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7ce7e-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7ce7e-106">Child elements</span></span>



| <span data-ttu-id="7ce7e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="7ce7e-107">Element</span></span>                                                                 | <span data-ttu-id="7ce7e-108">Type</span><span class="sxs-lookup"><span data-stu-id="7ce7e-108">Type</span></span>    | <span data-ttu-id="7ce7e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ce7e-109">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ce7e-110">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="7ce7e-110">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="7ce7e-111">booleano</span><span class="sxs-lookup"><span data-stu-id="7ce7e-111">boolean</span></span> | <span data-ttu-id="7ce7e-112">Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="7ce7e-112">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span><br/>       |
| [<span data-ttu-id="7ce7e-113">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="7ce7e-113">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="7ce7e-114">booleano</span><span class="sxs-lookup"><span data-stu-id="7ce7e-114">boolean</span></span> | <span data-ttu-id="7ce7e-115">Especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 X para autenticação de porta.</span><span class="sxs-lookup"><span data-stu-id="7ce7e-115">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="7ce7e-116">**segurança**</span><span class="sxs-lookup"><span data-stu-id="7ce7e-116">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="7ce7e-117">Contém configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="7ce7e-117">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="7ce7e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ce7e-118">Requirements</span></span>



| <span data-ttu-id="7ce7e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ce7e-119">Requirement</span></span> | <span data-ttu-id="7ce7e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7ce7e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7ce7e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ce7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce7e-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ce7e-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7ce7e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ce7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce7e-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ce7e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ce7e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ce7e-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="7ce7e-126">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="7ce7e-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7ce7e-127">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="7ce7e-127">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="7ce7e-128">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="7ce7e-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7ce7e-129">**LANProfile**</span><span class="sxs-lookup"><span data-stu-id="7ce7e-129">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




