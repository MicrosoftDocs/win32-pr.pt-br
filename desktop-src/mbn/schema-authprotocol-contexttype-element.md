---
description: Especifica o protocolo de autenticação a ser usado para ativar um contexto de protocolo de dados de pacote (PDP).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Elemento AuthProtocol (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784122"
---
# <a name="authprotocol-contexttype-element"></a><span data-ttu-id="19bb5-103">Elemento AuthProtocol (contextType)</span><span class="sxs-lookup"><span data-stu-id="19bb5-103">AuthProtocol (contextType) Element</span></span>

<span data-ttu-id="19bb5-104">O elemento **AuthProtocol (ContextType)** especifica o protocolo de autenticação a ser usado para ativar um contexto de protocolo de dados de pacote (PDP).</span><span class="sxs-lookup"><span data-stu-id="19bb5-104">The **AuthProtocol (contextType)** element specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="19bb5-105">O elemento pode ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="19bb5-105">The element can have one of the following values.</span></span>

| <span data-ttu-id="19bb5-106">Valor</span><span class="sxs-lookup"><span data-stu-id="19bb5-106">Value</span></span>      | <span data-ttu-id="19bb5-107">Significado</span><span class="sxs-lookup"><span data-stu-id="19bb5-107">Meaning</span></span>                                                                 |
|------------|-------------------------------------------------------------------------|
| <span data-ttu-id="19bb5-108">None</span><span class="sxs-lookup"><span data-stu-id="19bb5-108">"NONE"</span></span>     | <span data-ttu-id="19bb5-109">Nenhum protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="19bb5-109">No authentication protocol.</span></span>                                             |
| <span data-ttu-id="19bb5-110">PAP</span><span class="sxs-lookup"><span data-stu-id="19bb5-110">"PAP"</span></span>      | <span data-ttu-id="19bb5-111">Autenticação de senha não criptografada.</span><span class="sxs-lookup"><span data-stu-id="19bb5-111">Unencrypted password authentication.</span></span>                                    |
| <span data-ttu-id="19bb5-112">VIA</span><span class="sxs-lookup"><span data-stu-id="19bb5-112">"CHAP"</span></span>     | <span data-ttu-id="19bb5-113">CHAP (Challenge Handshake Authentication Protocol).</span><span class="sxs-lookup"><span data-stu-id="19bb5-113">Challenge Handshake Authentication Protocol(CHAP).</span></span>                      |
|  <span data-ttu-id="19bb5-114">MsCHAPV2</span><span class="sxs-lookup"><span data-stu-id="19bb5-114">MsCHAPV2"</span></span> | <span data-ttu-id="19bb5-115">Use o protocolo CHAP (Microsoft s Challenge Handshake Authentication Protocol) v 2.0.</span><span class="sxs-lookup"><span data-stu-id="19bb5-115">Use Microsoft s Challenge Handshake Authentication Protocol(CHAP) v2.0.</span></span> |



 

<span data-ttu-id="19bb5-116">Esse elemento é opcional e é usado somente para perfis GSM.</span><span class="sxs-lookup"><span data-stu-id="19bb5-116">This element is optional and is used only for GSM profiles.</span></span> <span data-ttu-id="19bb5-117">Se o elemento não for especificado e o perfil for para um dispositivo GSM, o serviço de banda larga móvel usará **"nenhum"**.</span><span class="sxs-lookup"><span data-stu-id="19bb5-117">If the element is not specified and the profile is for a GSM device, then the Mobile Broadband service will use **"NONE"**.</span></span>

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="19bb5-118">O elemento **AuthProtocol** é definido pelo tipo complexo [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="19bb5-118">The **AuthProtocol** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="19bb5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19bb5-119">Requirements</span></span>



| <span data-ttu-id="19bb5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="19bb5-120">Requirement</span></span> | <span data-ttu-id="19bb5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="19bb5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="19bb5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19bb5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="19bb5-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="19bb5-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="19bb5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19bb5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="19bb5-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="19bb5-125">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="19bb5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="19bb5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="19bb5-127">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="19bb5-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="19bb5-128">**contextType**</span><span class="sxs-lookup"><span data-stu-id="19bb5-128">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="19bb5-129">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="19bb5-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="19bb5-130">**Contexto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="19bb5-130">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




