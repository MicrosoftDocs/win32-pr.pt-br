---
description: Indica se uma chave compartilhada é criptografada.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: Elemento protected (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758744"
---
# <a name="protected-sharedkey-element"></a><span data-ttu-id="89c00-103">Elemento protected (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="89c00-103">protected (sharedKey) Element</span></span>

<span data-ttu-id="89c00-104">O elemento protected (sharedKey) indica se uma chave compartilhada é criptografada.</span><span class="sxs-lookup"><span data-stu-id="89c00-104">The protected (sharedKey) element indicates whether a shared key is encrypted.</span></span>

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

<span data-ttu-id="89c00-105">O elemento é definido pelo elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="89c00-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="89c00-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="89c00-106">Remarks</span></span>

<span data-ttu-id="89c00-107">Para o Windows Vista e o Windows Server 2008, o **protegido** sempre terá um valor de true se o perfil tiver sido recuperado do repositório de perfis (por exemplo, chamando [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span><span class="sxs-lookup"><span data-stu-id="89c00-107">For Windows Vista and Windows Server 2008, **protected** always has a value of TRUE if the profile was retrieved from the profile store (for example, by calling [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span></span>

<span data-ttu-id="89c00-108">Para perfis destinados a uso no Windows XP com Service Pack 3 (SP3) ou API de LAN sem fio para Windows XP com Service Pack 2 (SP2), **protegido** deve ter um valor de false.</span><span class="sxs-lookup"><span data-stu-id="89c00-108">For profiles intended for use on Windows XP with Service Pack 3 (SP3) or Wireless LAN API for Windows XP with Service Pack 2 (SP2), **protected** must have a value of FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="89c00-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="89c00-109">Examples</span></span>

<span data-ttu-id="89c00-110">Para exibir perfis de exemplo que usam o elemento **protegido** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="89c00-110">To view sample profiles that use the **protected** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89c00-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89c00-111">Requirements</span></span>



| <span data-ttu-id="89c00-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="89c00-112">Requirement</span></span> | <span data-ttu-id="89c00-113">Valor</span><span class="sxs-lookup"><span data-stu-id="89c00-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="89c00-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89c00-114">Minimum supported client</span></span><br/> | <span data-ttu-id="89c00-115">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="89c00-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89c00-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89c00-116">Minimum supported server</span></span><br/> | <span data-ttu-id="89c00-117">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89c00-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="89c00-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="89c00-118">Redistributable</span></span><br/>          | <span data-ttu-id="89c00-119">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="89c00-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="89c00-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="89c00-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="89c00-121">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="89c00-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="89c00-122">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="89c00-122">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="89c00-123">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="89c00-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="89c00-124">**sharedKey (segurança)**</span><span class="sxs-lookup"><span data-stu-id="89c00-124">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




