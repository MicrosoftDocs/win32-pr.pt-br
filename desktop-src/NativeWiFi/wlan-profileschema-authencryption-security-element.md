---
description: Especifica o par de autenticação e criptografia a ser usado para este perfil.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Elemento authEncryption (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754205"
---
# <a name="authencryption-security-element"></a><span data-ttu-id="1274b-103">Elemento authEncryption (segurança)</span><span class="sxs-lookup"><span data-stu-id="1274b-103">authEncryption (security) Element</span></span>

<span data-ttu-id="1274b-104">O elemento authEncryption (segurança) especifica o par de autenticação e criptografia a ser usado para esse perfil.</span><span class="sxs-lookup"><span data-stu-id="1274b-104">The authEncryption (security) element specifies the authentication and encryption pair to be used for this profile.</span></span>

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
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
```

<span data-ttu-id="1274b-105">O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1274b-105">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1274b-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1274b-106">Child elements</span></span>



| <span data-ttu-id="1274b-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="1274b-107">Element</span></span>                                                                            | <span data-ttu-id="1274b-108">Type</span><span class="sxs-lookup"><span data-stu-id="1274b-108">Type</span></span>                                                              | <span data-ttu-id="1274b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="1274b-109">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1274b-110">**Authentication**</span><span class="sxs-lookup"><span data-stu-id="1274b-110">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="1274b-111">Especifica o método de autenticação que deve ser usado para se conectar à LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="1274b-111">Specifies the authentication method that must be used to connect to the wireless LAN.</span></span><br/> |
| [<span data-ttu-id="1274b-112">**encripta**</span><span class="sxs-lookup"><span data-stu-id="1274b-112">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="1274b-113">Define a criptografia de dados a ser usada para se conectar à LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="1274b-113">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                       |
| [<span data-ttu-id="1274b-114">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="1274b-114">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="1274b-115">booleano</span><span class="sxs-lookup"><span data-stu-id="1274b-115">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="1274b-116">Indica se 802.1 X é usado.</span><span class="sxs-lookup"><span data-stu-id="1274b-116">Indicates whether 802.1X is used.</span></span><br/>                                                     |



## <a name="remarks"></a><span data-ttu-id="1274b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1274b-117">Remarks</span></span>

<span data-ttu-id="1274b-118">O elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) pode ser inserido como um filho do elemento **authEncryption** .</span><span class="sxs-lookup"><span data-stu-id="1274b-118">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the **authEncryption** element.</span></span>

## <a name="examples"></a><span data-ttu-id="1274b-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1274b-119">Examples</span></span>

<span data-ttu-id="1274b-120">Para exibir perfis de exemplo que usam o elemento **authEncryption** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="1274b-120">To view sample profiles that use the **authEncryption** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span> <span data-ttu-id="1274b-121">Para exibir um perfil de exemplo que usa o elemento [**fipsmode**](wlan-profileschema-fipsmode-authencryption-element.md) , consulte [exemplo de perfil FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1274b-121">To view a sample profile that uses the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1274b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1274b-122">Requirements</span></span>



| <span data-ttu-id="1274b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1274b-123">Requirement</span></span> | <span data-ttu-id="1274b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1274b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1274b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1274b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1274b-126">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="1274b-126">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1274b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1274b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1274b-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1274b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="1274b-129">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="1274b-129">Redistributable</span></span><br/>          | <span data-ttu-id="1274b-130">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="1274b-130">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1274b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="1274b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1274b-132">Exemplos de perfil sem fio</span><span class="sxs-lookup"><span data-stu-id="1274b-132">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="1274b-133">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="1274b-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1274b-134">**segurança**</span><span class="sxs-lookup"><span data-stu-id="1274b-134">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="1274b-135">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="1274b-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1274b-136">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="1274b-136">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
