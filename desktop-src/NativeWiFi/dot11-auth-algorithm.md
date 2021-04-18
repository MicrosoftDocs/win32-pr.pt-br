---
description: Define um algoritmo de autenticação de LAN sem fio.
ms.assetid: ac4097df-46dc-4c64-b72a-7cb9dce8b418
title: Enumeração de DOT11_AUTH_ALGORITHM (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 1b14886c62448194b79eab2e0302ce5608ad282d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770153"
---
# <a name="dot11_auth_algorithm-enumeration"></a><span data-ttu-id="c5ff2-103">Enumeração de algoritmo de \_ autenticação DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="c5ff2-103">DOT11\_AUTH\_ALGORITHM enumeration</span></span>

<span data-ttu-id="c5ff2-104">O tipo enumerado do **\_ \_ algoritmo DOT11 auth** define um algoritmo de autenticação de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-104">The **DOT11\_AUTH\_ALGORITHM** enumerated type defines a wireless LAN authentication algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ff2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5ff2-105">Syntax</span></span>


```C++
typedef enum _DOT11_AUTH_ALGORITHM { 
  DOT11_AUTH_ALGO_80211_OPEN        = 1,
  DOT11_AUTH_ALGO_80211_SHARED_KEY  = 2,
  DOT11_AUTH_ALGO_WPA               = 3,
  DOT11_AUTH_ALGO_WPA_PSK           = 4,
  DOT11_AUTH_ALGO_WPA_NONE          = 5,
  DOT11_AUTH_ALGO_RSNA              = 6,
  DOT11_AUTH_ALGO_RSNA_PSK          = 7,
  DOT11_AUTH_ALGO_IHV_START         = 0x80000000,
  DOT11_AUTH_ALGO_IHV_END           = 0xffffffff
} DOT11_AUTH_ALGORITHM, *PDOT11_AUTH_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="c5ff2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c5ff2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c5ff2-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11 \_ auth \_ algo \_ 80211 \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-107"><span id="DOT11_AUTH_ALGO_80211_OPEN"></span><span id="dot11_auth_algo_80211_open"></span>**DOT11\_AUTH\_ALGO\_80211\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-108">Especifica um algoritmo de autenticação do sistema aberto IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-108">Specifies an IEEE 802.11 Open System authentication algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff2-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**\_Chave compartilhada DOT11 auth \_ algo \_ 80211 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-109"><span id="DOT11_AUTH_ALGO_80211_SHARED_KEY"></span><span id="dot11_auth_algo_80211_shared_key"></span>**DOT11\_AUTH\_ALGO\_80211\_SHARED\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-110">Especifica um algoritmo de autenticação de chave compartilhada 802,11 que requer o uso de uma chave WEP (Wired Equivalent Privacy) pré-compartilhada para a autenticação 802,11.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-110">Specifies an 802.11 Shared Key authentication algorithm that requires the use of a pre-shared Wired Equivalent Privacy (WEP) key for the 802.11 authentication.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff2-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**\_WPA de \_ algo de autenticação DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-111"><span id="DOT11_AUTH_ALGO_WPA"></span><span id="dot11_auth_algo_wpa"></span>**DOT11\_AUTH\_ALGO\_WPA**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-112">Especifica um algoritmo de WPA (acesso protegido Wi-Fi).</span><span class="sxs-lookup"><span data-stu-id="c5ff2-112">Specifies a Wi-Fi Protected Access (WPA) algorithm.</span></span> <span data-ttu-id="c5ff2-113">A autenticação de porta IEEE 802.1 X é executada pelo suplicante, autenticador e servidor de autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-113">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="c5ff2-114">As chaves de codificação são derivadas dinamicamente por meio do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-114">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="c5ff2-115">Esse algoritmo é válido somente para tipos de BSS da \_ infraestrutura de tipo BSS dot11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c5ff2-115">This algorithm is valid only for BSS types of dot11\_BSS\_type\_infrastructure.</span></span>

<span data-ttu-id="c5ff2-116">Quando o algoritmo WPA estiver habilitado, a estação 802,11 será associada somente a um ponto de acesso cujas respostas de Beacon ou Probe contenham o conjunto de autenticação do tipo 1 (802.1 X) no elemento de informações WPA (ou seja).</span><span class="sxs-lookup"><span data-stu-id="c5ff2-116">When the WPA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the WPA information element (IE).</span></span>

</dd> <dt>

<span data-ttu-id="c5ff2-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11 \_ auth \_ algo \_ WPA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-117"><span id="DOT11_AUTH_ALGO_WPA_PSK"></span><span id="dot11_auth_algo_wpa_psk"></span>**DOT11\_AUTH\_ALGO\_WPA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-118">Especifica um algoritmo WPA que usa chaves pré-compartilhadas (PSK).</span><span class="sxs-lookup"><span data-stu-id="c5ff2-118">Specifies a WPA algorithm that uses preshared keys (PSK).</span></span> <span data-ttu-id="c5ff2-119">A autenticação de porta IEEE 802.1 X é executada pelo suplicante e pelo autenticador.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-119">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="c5ff2-120">As chaves de codificação são derivadas dinamicamente por meio de uma chave pré-compartilhada que é usada no suplicante e no autenticador.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-120">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="c5ff2-121">Esse algoritmo é válido somente para tipos de BSS **da \_ \_ \_ infraestrutura de tipo BSS dot11**.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-121">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="c5ff2-122">Quando o algoritmo WPA PSK estiver habilitado, a estação 802,11 será associada somente a um ponto de acesso cujas respostas de Beacon ou investigação contenham o conjunto de autenticação do tipo 2 (chave pré-compartilhada) no IE do WPA.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-122">When the WPA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2 (preshared key) within the WPA IE.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff2-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11 \_ auth \_ algo \_ WPA \_ None**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-123"><span id="DOT11_AUTH_ALGO_WPA_NONE"></span><span id="dot11_auth_algo_wpa_none"></span>**DOT11\_AUTH\_ALGO\_WPA\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-124">Não há suporte para esse valor.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-124">This value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff2-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**\_Algo de autenticação DOT11 \_ \_ RSNA**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-125"><span id="DOT11_AUTH_ALGO_RSNA"></span><span id="dot11_auth_algo_rsna"></span>**DOT11\_AUTH\_ALGO\_RSNA**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-126">Especifica um algoritmo RSNA (Associação de rede de segurança robusta) 802.11.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-126">Specifies an 802.11i Robust Security Network Association (RSNA) algorithm.</span></span> <span data-ttu-id="c5ff2-127">O WPA2 é um desses algoritmos.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-127">WPA2 is one such algorithm.</span></span> <span data-ttu-id="c5ff2-128">A autenticação de porta IEEE 802.1 X é executada pelo suplicante, autenticador e servidor de autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-128">IEEE 802.1X port authentication is performed by the supplicant, authenticator, and authentication server.</span></span> <span data-ttu-id="c5ff2-129">As chaves de codificação são derivadas dinamicamente por meio do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-129">Cipher keys are dynamically derived through the authentication process.</span></span>

<span data-ttu-id="c5ff2-130">Esse algoritmo é válido somente para tipos de BSS **da \_ \_ \_ infraestrutura de tipo BSS dot11**.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-130">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="c5ff2-131">Quando o algoritmo RSNA estiver habilitado, a estação 802,11 será associada somente a um ponto de acesso cujas respostas de Beacon ou Probe contenham o conjunto de autenticação do tipo 1 (802.1 X) dentro do RSN IE.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-131">When the RSNA algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 1 (802.1X) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff2-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11 \_ auth \_ algo \_ RSNA \_ PSK**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-132"><span id="DOT11_AUTH_ALGO_RSNA_PSK"></span><span id="dot11_auth_algo_rsna_psk"></span>**DOT11\_AUTH\_ALGO\_RSNA\_PSK**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-133">Especifica um algoritmo 802.11 i RSNA que usa PSK.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-133">Specifies an 802.11i RSNA algorithm that uses PSK.</span></span> <span data-ttu-id="c5ff2-134">A autenticação de porta IEEE 802.1 X é executada pelo suplicante e pelo autenticador.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-134">IEEE 802.1X port authentication is performed by the supplicant and authenticator.</span></span> <span data-ttu-id="c5ff2-135">As chaves de codificação são derivadas dinamicamente por meio de uma chave pré-compartilhada que é usada no suplicante e no autenticador.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-135">Cipher keys are dynamically derived through a preshared key that is used on both the supplicant and authenticator.</span></span>

<span data-ttu-id="c5ff2-136">Esse algoritmo é válido somente para tipos de BSS **da \_ \_ \_ infraestrutura de tipo BSS dot11**.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-136">This algorithm is valid only for BSS types of **dot11\_BSS\_type\_infrastructure**.</span></span>

<span data-ttu-id="c5ff2-137">Quando o algoritmo PSK RSNA estiver habilitado, a estação 802,11 será associada somente a um ponto de acesso cujas respostas de Beacon ou investigação contenham o conjunto de autenticação do tipo 2 (chave pré-compartilhada) dentro do RSN IE.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-137">When the RSNA PSK algorithm is enabled, the 802.11 station will associate only with an access point whose beacon or probe responses contain the authentication suite of type 2(preshared key) within the RSN IE.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff2-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**\_Início do IHV da autenticação DOT11 \_ algo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-138"><span id="DOT11_AUTH_ALGO_IHV_START"></span><span id="dot11_auth_algo_ihv_start"></span>**DOT11\_AUTH\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-139">Indica o início do intervalo que especifica os algoritmos de autenticação proprietários desenvolvidos por um IHV.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-139">Indicates the start of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="c5ff2-140">O enumerador de **\_ inicialização DOT11 auth \_ algo \_ IHV \_** é válido somente quando o driver de miniporta está operando no modo de estação extensível (ExtSTA).</span><span class="sxs-lookup"><span data-stu-id="c5ff2-140">The **DOT11\_AUTH\_ALGO\_IHV\_START** enumerator is valid only when the miniport driver is operating in Extensible Station (ExtSTA) mode.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff2-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**\_Fim de IHV da autenticação DOT11 \_ algo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-141"><span id="DOT11_AUTH_ALGO_IHV_END"></span><span id="dot11_auth_algo_ihv_end"></span>**DOT11\_AUTH\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="c5ff2-142">Indica o final do intervalo que especifica os algoritmos de autenticação proprietários que são desenvolvidos por um IHV.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-142">Indicates the end of the range that specifies proprietary authentication algorithms that are developed by an IHV.</span></span>

<span data-ttu-id="c5ff2-143">O enumerador de **\_ \_ \_ \_ extremidade de IHV algo DOT11 auth** é válido somente quando o driver de miniporta está operando no modo ExtSTA.</span><span class="sxs-lookup"><span data-stu-id="c5ff2-143">The **DOT11\_AUTH\_ALGO\_IHV\_END** enumerator is valid only when the miniport driver is operating in ExtSTA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5ff2-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5ff2-144">Requirements</span></span>



| <span data-ttu-id="c5ff2-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ff2-145">Requirement</span></span> | <span data-ttu-id="c5ff2-146">Valor</span><span class="sxs-lookup"><span data-stu-id="c5ff2-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ff2-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5ff2-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ff2-148">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="c5ff2-148">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c5ff2-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5ff2-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ff2-150">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5ff2-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="c5ff2-151">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c5ff2-151">Redistributable</span></span><br/>          | <span data-ttu-id="c5ff2-152">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="c5ff2-152">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="c5ff2-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5ff2-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ff2-154"><dt>Wlantypes. h (incluir Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff2-154"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ff2-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5ff2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ff2-156">**Par de codificação de DOT11 \_ auth \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-156">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="c5ff2-157">**rede de WLAN \_ disponível \_**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-157">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="c5ff2-158">**\_atributos de segurança de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="c5ff2-158">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




