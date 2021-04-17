---
description: Especifica as informações de configuração de rede de logon único (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Elemento logon único (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787050"
---
# <a name="singlesignon-onex-element"></a><span data-ttu-id="4c758-103">Elemento logon único (OneX)</span><span class="sxs-lookup"><span data-stu-id="4c758-103">singleSignOn (OneX) Element</span></span>

<span data-ttu-id="4c758-104">O elemento logon único (OneX) especifica as informações de configuração de rede de logon único (SSO).</span><span class="sxs-lookup"><span data-stu-id="4c758-104">The singleSignOn (OneX) element specifies single sign-on (SSO) network configuration information.</span></span>

<span data-ttu-id="4c758-105">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="4c758-105">This element is optional.</span></span> <span data-ttu-id="4c758-106">Não use o elemento logon único em um perfil se a rede não o exigir.</span><span class="sxs-lookup"><span data-stu-id="4c758-106">Do not use the singleSignOn element in a profile if the network does not require it.</span></span>

<span data-ttu-id="4c758-107">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.</span><span class="sxs-lookup"><span data-stu-id="4c758-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4c758-108">O elemento **logon único** é definido pelo elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4c758-108">The **singleSignOn** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4c758-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4c758-109">Child elements</span></span>



| <span data-ttu-id="4c758-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="4c758-110">Element</span></span>                                                                            | <span data-ttu-id="4c758-111">Type</span><span class="sxs-lookup"><span data-stu-id="4c758-111">Type</span></span>    | <span data-ttu-id="4c758-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c758-112">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c758-113">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="4c758-113">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="4c758-114">Especifica, em segundos, o atraso máximo antes da tentativa de conexão de logon único falhar.</span><span class="sxs-lookup"><span data-stu-id="4c758-114">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="4c758-115">**Escreva**</span><span class="sxs-lookup"><span data-stu-id="4c758-115">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="4c758-116">Especifica quando o logon único é executado.</span><span class="sxs-lookup"><span data-stu-id="4c758-116">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="4c758-117">Quando definido como `preLogon` , o logon único é executado antes de o usuário fazer logon.</span><span class="sxs-lookup"><span data-stu-id="4c758-117">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="4c758-118">Quando definido como `postLogon` , o logon único é executado imediatamente após o usuário fazer logon.</span><span class="sxs-lookup"><span data-stu-id="4c758-118">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="4c758-119">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="4c758-119">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="4c758-120">booleano</span><span class="sxs-lookup"><span data-stu-id="4c758-120">boolean</span></span> | <span data-ttu-id="4c758-121">Especifica se a LAN virtual (VLAN) usada pelo dispositivo é alterada com base nas credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="4c758-121">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="4c758-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c758-122">Remarks</span></span>

<span data-ttu-id="4c758-123">Esse parâmetro pode ser definido na linha de comando usando o comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="4c758-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="4c758-124">Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="4c758-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c758-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c758-125">Requirements</span></span>



| <span data-ttu-id="4c758-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c758-126">Requirement</span></span> | <span data-ttu-id="4c758-127">Valor</span><span class="sxs-lookup"><span data-stu-id="4c758-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c758-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c758-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4c758-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c758-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c758-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c758-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4c758-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c758-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c758-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c758-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c758-133">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="4c758-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4c758-134">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="4c758-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="4c758-135">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="4c758-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4c758-136">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="4c758-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
