---
description: Contém várias configurações de segurança usadas por fornecedores de hardware independentes.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Elemento de segurança (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770150"
---
# <a name="security-ihv-element"></a><span data-ttu-id="a4b42-103">Elemento de segurança (IHV)</span><span class="sxs-lookup"><span data-stu-id="a4b42-103">security (IHV) Element</span></span>

<span data-ttu-id="a4b42-104">O elemento de segurança (IHV) contém várias configurações de segurança usadas por fornecedores de hardware independentes.</span><span class="sxs-lookup"><span data-stu-id="a4b42-104">The security (IHV) element contains various security settings used by independent hardware vendors.</span></span>

<span data-ttu-id="a4b42-105">As configurações de segurança da Microsoft e as configurações de segurança de IHV são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="a4b42-105">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="a4b42-106">Se os dois conjuntos de configurações de segurança estiverem presentes no mesmo perfil, o perfil será inválido.</span><span class="sxs-lookup"><span data-stu-id="a4b42-106">If both sets of security settings are present in the same profile, the profile is invalid.</span></span>

<span data-ttu-id="a4b42-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="a4b42-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a4b42-108">O elemento **Security** é definido pelo elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a4b42-108">The **security** element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b42-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4b42-109">Requirements</span></span>



| <span data-ttu-id="a4b42-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b42-110">Requirement</span></span> | <span data-ttu-id="a4b42-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a4b42-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4b42-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4b42-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b42-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4b42-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4b42-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4b42-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b42-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4b42-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4b42-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4b42-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4b42-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a4b42-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a4b42-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="a4b42-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a4b42-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a4b42-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a4b42-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="a4b42-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




