---
description: Especifica o tipo de criptografia de dados a ser usado para se conectar a uma LAN sem fio.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Elemento Encryption (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090661"
---
# <a name="encryption-authencryption-element"></a><span data-ttu-id="019b6-103">Elemento Encryption (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="019b6-103">encryption (authEncryption) Element</span></span>

<span data-ttu-id="019b6-104">O elemento Encryption (authEncryption) especifica o tipo de criptografia de dados a ser usado para se conectar a uma LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="019b6-104">The encryption (authEncryption) element specifies the type of data encryption to use to connect to a wireless LAN.</span></span>

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="019b6-105">O elemento é definido pelo elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="019b6-105">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="019b6-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="019b6-106">Remarks</span></span>

<span data-ttu-id="019b6-107">Quando o elemento **Encryption** tem um valor de WEP, [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) deve ser definido como **networkKey**.</span><span class="sxs-lookup"><span data-stu-id="019b6-107">When the **encryption** element has a value of WEP, [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) must be set to **networkKey**.</span></span>

<span data-ttu-id="019b6-108">O método de criptografia AES é conforme especificado nas especificações [802.1 x](https://ieeexplore.ieee.org/document/1438730) e [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .</span><span class="sxs-lookup"><span data-stu-id="019b6-108">The AES encryption method is as specified in the [802.1X](https://ieeexplore.ieee.org/document/1438730) and [802.11i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) specifications.</span></span>

## <a name="examples"></a><span data-ttu-id="019b6-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="019b6-109">Examples</span></span>

<span data-ttu-id="019b6-110">Para exibir perfis de exemplo que usam o elemento de **criptografia** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="019b6-110">To view sample profiles that use the **encryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="019b6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="019b6-111">Requirements</span></span>



| <span data-ttu-id="019b6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="019b6-112">Requirement</span></span> | <span data-ttu-id="019b6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="019b6-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="019b6-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="019b6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="019b6-115">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="019b6-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="019b6-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="019b6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="019b6-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="019b6-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="019b6-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="019b6-118">Redistributable</span></span><br/>          | <span data-ttu-id="019b6-119">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="019b6-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="019b6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="019b6-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="019b6-121">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="019b6-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="019b6-122">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="019b6-122">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="019b6-123">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="019b6-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="019b6-124">**authEncryption (segurança)**</span><span class="sxs-lookup"><span data-stu-id="019b6-124">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




