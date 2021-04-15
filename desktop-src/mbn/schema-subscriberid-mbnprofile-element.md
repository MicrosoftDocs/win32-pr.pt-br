---
description: Identifica o identificador exclusivo do perfil.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Elemento subscriberid (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501844"
---
# <a name="subscriberid-mbnprofile-element"></a><span data-ttu-id="d6145-103">Elemento subscriberid (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="d6145-103">SubscriberID (MBNProfile) Element</span></span>

<span data-ttu-id="d6145-104">O elemento **subscriberid (MBNProfile)** identifica o identificador exclusivo do perfil.</span><span class="sxs-lookup"><span data-stu-id="d6145-104">The **SubscriberID (MBNProfile)** element identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="d6145-105">Para uma rede GSM, isso deve conter a IMSI (identidade do assinante internacional móvel) do SIM e para dispositivos CDMA que ele deve conter o mínimo (número de identificação móvel) do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d6145-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="d6145-106">O elemento é uma cadeia de caracteres numérica com um comprimento máximo de 15 dígitos.</span><span class="sxs-lookup"><span data-stu-id="d6145-106">The element is is a numeric string with a maximum length 15 digits.</span></span>

<span data-ttu-id="d6145-107">O elemento é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="d6145-107">The element is required.</span></span>

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

<span data-ttu-id="d6145-108">O elemento **subscriberid** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d6145-108">The **SubscriberID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6145-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6145-109">Requirements</span></span>



| <span data-ttu-id="d6145-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6145-110">Requirement</span></span> | <span data-ttu-id="d6145-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d6145-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d6145-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6145-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d6145-113">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6145-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d6145-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6145-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d6145-115">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d6145-115">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d6145-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6145-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6145-117">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="d6145-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d6145-118">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d6145-118">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="d6145-119">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="d6145-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d6145-120">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d6145-120">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




