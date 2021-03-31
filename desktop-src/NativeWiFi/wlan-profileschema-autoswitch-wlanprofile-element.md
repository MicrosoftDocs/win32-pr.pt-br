---
description: Determina o comportamento de roaming de uma rede conectada automaticamente quando uma rede preferencial está no intervalo.
ms.assetid: 095dc797-1249-43aa-a8b7-5fa6eaee2a74
title: Elemento AutoSwitch (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- autoSwitch
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7ae05b18f58927e05c952edbbfc1b6a6190cec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827503"
---
# <a name="autoswitch-wlanprofile-element"></a><span data-ttu-id="3afd4-103">Elemento AutoSwitch (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="3afd4-103">autoSwitch (WLANProfile) Element</span></span>

<span data-ttu-id="3afd4-104">O elemento AutoSwitch (WLANProfile) determina o comportamento de roaming de uma rede conectada automaticamente quando uma rede preferencial está no intervalo.</span><span class="sxs-lookup"><span data-stu-id="3afd4-104">The autoSwitch (WLANProfile) element determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="3afd4-105">.</span><span class="sxs-lookup"><span data-stu-id="3afd4-105">.</span></span> <span data-ttu-id="3afd4-106">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="3afd4-106">This element is optional.</span></span>

<span data-ttu-id="3afd4-107">Se AutoSwitch for "true" e [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) for definido como "auto", uma conexão com uma rede preferencial deverá ser tentada sempre que uma rede preferencial entrar em intervalo.</span><span class="sxs-lookup"><span data-stu-id="3afd4-107">If autoSwitch is "true" and [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", a connection to a more preferred network must be attempted whenever a more preferred network comes into range.</span></span> <span data-ttu-id="3afd4-108">Uma rede mais preferencial é aquela que é ordenada mais alta na lista de redes sem fio preferenciais.</span><span class="sxs-lookup"><span data-stu-id="3afd4-108">A more preferred network is one that is ordered higher in the list of preferred wireless networks.</span></span> <span data-ttu-id="3afd4-109">Essa tentativa de conexão ocorre quando conectado a outra rede.</span><span class="sxs-lookup"><span data-stu-id="3afd4-109">This connection attempt occurs when connected to another network.</span></span>

<span data-ttu-id="3afd4-110">Se [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) for definido como "auto", esse valor poderá ser "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="3afd4-110">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "auto", this value can be either "true" or "false".</span></span>

<span data-ttu-id="3afd4-111">Se [**ConnectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) for definido como "manual", esse valor deverá ser definido como "false".</span><span class="sxs-lookup"><span data-stu-id="3afd4-111">If [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md) is set to "manual", this value must be set to "false".</span></span> <span data-ttu-id="3afd4-112">Este elemento não tem nenhum efeito em uma rede conectada manualmente.</span><span class="sxs-lookup"><span data-stu-id="3afd4-112">This element has no effect on a manually connected network.</span></span>

<span data-ttu-id="3afd4-113">Um valor de comutador AutoSwitch definido como "true" resulta em uma frequência mais alta de verificação periódica para novas redes.</span><span class="sxs-lookup"><span data-stu-id="3afd4-113">An autoSwitch value set to "true" results in a higher frequency of periodic scanning for new networks.</span></span> <span data-ttu-id="3afd4-114">Isso pode resultar na maior poluição da freqüência de rádio dessas verificações periódicas e ao aumento do consumo de energia usado pelo adaptador de rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="3afd4-114">This may result in increased radio frequency pollution from these periodic scans and increased power consumption used by the wireless network adapter.</span></span>

<span data-ttu-id="3afd4-115">**Windows 7 e Windows Server 2008 R2 com o serviço de LAN sem fio instalado:** As alterações são implementadas no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado para otimizar o desempenho da rede sem fio.</span><span class="sxs-lookup"><span data-stu-id="3afd4-115">**Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed:** Changes are implemented on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed to optimize wireless networking performance.</span></span> <span data-ttu-id="3afd4-116">Essas alterações foram projetadas para reduzir a poluição da frequência de rádio, o consumo de energia e a interrupção no tráfego em tempo real em redes sem fio.</span><span class="sxs-lookup"><span data-stu-id="3afd4-116">These changes are designed to reduce radio frequency pollution, power consumption, and disruption to real-time traffic over wireless networks.</span></span> <span data-ttu-id="3afd4-117">A configuração padrão para **AutoSwitch** quando este elemento não está definido em um perfil de LAN sem fio foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3afd4-117">The default setting for **autoSwitch** when this element is not set in a wireless LAN profile has changed.</span></span> <span data-ttu-id="3afd4-118">A configuração padrão é alterada para "false" no Windows 7 e no Windows Server 2008 R2 com o serviço de LAN sem fio instalado.</span><span class="sxs-lookup"><span data-stu-id="3afd4-118">The default setting is changed to "false" on Windows 7 and Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span> <span data-ttu-id="3afd4-119">A configuração padrão era "true" no Windows Server 2008 e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3afd4-119">The default setting was "true" on Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="3afd4-120">É recomendável que o valor do elemento de **comutador AutoSwitch** usado por um aplicativo em um perfil de LAN sem fio seja definido como "false" para reduzir a frequência de verificação periódica para novas redes, a menos que seja absolutamente necessário para um aplicativo definir esse valor como "true".</span><span class="sxs-lookup"><span data-stu-id="3afd4-120">It is recommended that the value of the **autoSwitch** element used by an application in a wireless LAN profile be set to "false" to reduce the frequency of periodic scanning for new networks, unless it is absolutely necessary for an application to set this value to "true".</span></span>

<span data-ttu-id="3afd4-121">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="3afd4-121">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="autoSwitch"
    type="boolean"
 />
```

<span data-ttu-id="3afd4-122">O elemento **AutoSwitch** é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3afd4-122">The **autoSwitch** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="3afd4-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3afd4-123">Examples</span></span>

<span data-ttu-id="3afd4-124">Para exibir perfis de exemplo que usam o elemento **AutoSwitch** , consulte [amostras de perfil sem fio](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="3afd4-124">To view sample profiles that use the **autoSwitch** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3afd4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3afd4-125">Requirements</span></span>



| <span data-ttu-id="3afd4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3afd4-126">Requirement</span></span> | <span data-ttu-id="3afd4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3afd4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3afd4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3afd4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3afd4-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3afd4-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3afd4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3afd4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3afd4-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3afd4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3afd4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3afd4-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="3afd4-133">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="3afd4-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3afd4-134">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="3afd4-134">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="3afd4-135">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="3afd4-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3afd4-136">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="3afd4-136">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




