---
description: Especifica se o dispositivo de banda larga móvel se conectará automaticamente a uma rede.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Elemento AutoConnectOnInternet (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164576"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a><span data-ttu-id="04ac5-103">Elemento AutoConnectOnInternet (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="04ac5-103">AutoConnectOnInternet (MBNProfile) Element</span></span>

<span data-ttu-id="04ac5-104">O elemento **AutoConnectOnInternet (MBNProfile)** especifica se o dispositivo de banda larga móvel se conectará automaticamente a uma rede.</span><span class="sxs-lookup"><span data-stu-id="04ac5-104">The **AutoConnectOnInternet (MBNProfile)** element specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="04ac5-105">Se definido como **false**, a lógica de conexão automática do serviço de banda larga móvel não será usada se houver qualquer outra conectividade de rede disponível para o sistema.</span><span class="sxs-lookup"><span data-stu-id="04ac5-105">If set to **FALSE**, then the Mobile Broadband service's auto connect logic will not be used if there is any other network connectivity available to the system.</span></span> <span data-ttu-id="04ac5-106">Se definido como **true**, o serviço de banda larga móvel tentará conectar automaticamente o dispositivo à rede com base na configuração de conexão automática definida no elemento [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="04ac5-106">If set to **TRUE**, then the Mobile Broadband service will try to automatically connect the device to the network based on the auto connection setting defined in the [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) element.</span></span>

<span data-ttu-id="04ac5-107">**Windows 8 e posterior:** Este elemento foi preterido.</span><span class="sxs-lookup"><span data-stu-id="04ac5-107">**Windows 8 and later:** This element is deprecated.</span></span> <span data-ttu-id="04ac5-108">Use o método [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) com o parâmetro *Property* definido como **WCM \_ \_ propriedade global \_ minimizar \_ política** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="04ac5-108">Use the [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) method with the *Property* parameter set to **wcm\_global\_property\_minimize\_policy** instead.</span></span>

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

<span data-ttu-id="04ac5-109">O elemento **AutoConnectOnInternet** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="04ac5-109">The **AutoConnectOnInternet** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ac5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ac5-110">Requirements</span></span>



| <span data-ttu-id="04ac5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ac5-111">Requirement</span></span> | <span data-ttu-id="04ac5-112">Valor</span><span class="sxs-lookup"><span data-stu-id="04ac5-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="04ac5-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04ac5-113">Minimum supported client</span></span><br/> | <span data-ttu-id="04ac5-114">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="04ac5-114">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="04ac5-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04ac5-115">Minimum supported server</span></span><br/> | <span data-ttu-id="04ac5-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="04ac5-116">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="04ac5-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="04ac5-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="04ac5-118">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="04ac5-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="04ac5-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="04ac5-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="04ac5-120">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="04ac5-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="04ac5-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="04ac5-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

