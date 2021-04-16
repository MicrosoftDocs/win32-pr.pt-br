---
description: Indica se a chave compartilhada será uma chave de rede ou uma frase secreta.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: Elemento KeyType (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789631"
---
# <a name="keytype-sharedkey-element"></a><span data-ttu-id="22679-103">Elemento KeyType (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="22679-103">keyType (sharedKey) Element</span></span>

<span data-ttu-id="22679-104">O elemento KeyType (sharedKey) indica se a chave compartilhada será uma chave de rede ou uma frase secreta.</span><span class="sxs-lookup"><span data-stu-id="22679-104">The keyType (sharedKey) element indicates whether the shared key will be a network key or a pass phrase.</span></span>

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="22679-105">O elemento é definido pelo elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="22679-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="22679-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="22679-106">Remarks</span></span>

<span data-ttu-id="22679-107">Quando o elemento [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) tem um valor de WEP, **KeyType** deve ser definido como **networkKey**.</span><span class="sxs-lookup"><span data-stu-id="22679-107">When the [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of WEP, **keyType** must be set to **networkKey**.</span></span>

## <a name="examples"></a><span data-ttu-id="22679-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22679-108">Examples</span></span>

<span data-ttu-id="22679-109">Para exibir perfis de exemplo que usam o elemento **KeyType** , consulte exemplo de [perfil sem difusão](non-broadcast-profile-sample.md), [exemplo de perfil WPA-Pessoal](wpa-personal-profile-sample.md)e [exemplo de perfil WPA2-Pessoal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="22679-109">To view sample profiles that use the **keyType** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22679-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22679-110">Requirements</span></span>



| <span data-ttu-id="22679-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="22679-111">Requirement</span></span> | <span data-ttu-id="22679-112">Valor</span><span class="sxs-lookup"><span data-stu-id="22679-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="22679-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22679-113">Minimum supported client</span></span><br/> | <span data-ttu-id="22679-114">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="22679-114">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="22679-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22679-115">Minimum supported server</span></span><br/> | <span data-ttu-id="22679-116">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22679-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="22679-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="22679-117">Redistributable</span></span><br/>          | <span data-ttu-id="22679-118">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="22679-118">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="22679-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="22679-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="22679-120">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="22679-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="22679-121">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="22679-121">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="22679-122">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="22679-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="22679-123">**sharedKey (segurança)**</span><span class="sxs-lookup"><span data-stu-id="22679-123">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




