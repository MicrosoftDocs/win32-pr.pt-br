---
description: Contém informações de chave compartilhada.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: Elemento sharedKey (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754322"
---
# <a name="sharedkey-security-element"></a><span data-ttu-id="1de98-103">Elemento sharedKey (segurança)</span><span class="sxs-lookup"><span data-stu-id="1de98-103">sharedKey (security) Element</span></span>

<span data-ttu-id="1de98-104">O elemento sharedKey (Security) contém informações de chave compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="1de98-104">The sharedKey (security) element contains shared key information.</span></span> <span data-ttu-id="1de98-105">Esse elemento só será necessário se as chaves WEP ou PSK forem necessárias para o par de autenticação e criptografia.</span><span class="sxs-lookup"><span data-stu-id="1de98-105">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span>

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
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

<span data-ttu-id="1de98-106">O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1de98-106">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="1de98-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="1de98-107">Child elements</span></span>



| <span data-ttu-id="1de98-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="1de98-108">Element</span></span>                                                                 | <span data-ttu-id="1de98-109">Type</span><span class="sxs-lookup"><span data-stu-id="1de98-109">Type</span></span>                                                              | <span data-ttu-id="1de98-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1de98-110">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1de98-111">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="1de98-111">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md) | [<span data-ttu-id="1de98-112">cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="1de98-112">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="1de98-113">Contém a chave de rede ou frase secreta.</span><span class="sxs-lookup"><span data-stu-id="1de98-113">Contains the network key or passphrase.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="1de98-114">**keyType**</span><span class="sxs-lookup"><span data-stu-id="1de98-114">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | <span data-ttu-id="1de98-115">Tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="1de98-115">Type of key.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="1de98-116">**protected**</span><span class="sxs-lookup"><span data-stu-id="1de98-116">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)     | [<span data-ttu-id="1de98-117">booleano</span><span class="sxs-lookup"><span data-stu-id="1de98-117">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="1de98-118">Indica se a chave está criptografada.</span><span class="sxs-lookup"><span data-stu-id="1de98-118">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="1de98-119">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento deve ter um valor de FALSE.</span><span class="sxs-lookup"><span data-stu-id="1de98-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1de98-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1de98-120">Remarks</span></span>

<span data-ttu-id="1de98-121">Para o Windows Vista e o Windows Server 2008, os dados associados ao elemento **sharedKey** são criptografados antes de serem salvos no repositório de perfis.</span><span class="sxs-lookup"><span data-stu-id="1de98-121">For Windows Vista and Windows Server 2008, the data associated with the **sharedKey** element is encrypted before it is saved in the profile store.</span></span>

<span data-ttu-id="1de98-122">Para o Windows XP com SP3 e a API de LAN sem fio para Windows XP com SP2, os dados não são criptografados.</span><span class="sxs-lookup"><span data-stu-id="1de98-122">For Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, the data is not encrypted.</span></span>

## <a name="examples"></a><span data-ttu-id="1de98-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1de98-123">Examples</span></span>

<span data-ttu-id="1de98-124">Para exibir perfis de exemplo que usam o elemento **sharedKey** , consulte exemplo de [perfil sem difusão](non-broadcast-profile-sample.md), [exemplo de perfil WPA-Pessoal](wpa-personal-profile-sample.md)e [exemplo de perfil WPA2-Pessoal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1de98-124">To view sample profiles that use the **sharedKey** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1de98-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1de98-125">Requirements</span></span>



| <span data-ttu-id="1de98-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1de98-126">Requirement</span></span> | <span data-ttu-id="1de98-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1de98-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1de98-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1de98-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1de98-129">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="1de98-129">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1de98-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1de98-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1de98-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1de98-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="1de98-132">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="1de98-132">Redistributable</span></span><br/>          | <span data-ttu-id="1de98-133">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="1de98-133">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1de98-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1de98-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="1de98-135">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="1de98-135">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1de98-136">**segurança**</span><span class="sxs-lookup"><span data-stu-id="1de98-136">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="1de98-137">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="1de98-137">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1de98-138">**segurança (MSM)**</span><span class="sxs-lookup"><span data-stu-id="1de98-138">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
