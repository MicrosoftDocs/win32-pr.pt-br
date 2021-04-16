---
description: Define um algoritmo de codificação para criptografia e descriptografia de dados.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: Enumeração de DOT11_CIPHER_ALGORITHM (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759193"
---
# <a name="dot11_cipher_algorithm-enumeration"></a><span data-ttu-id="e2c0a-103">Enumeração de algoritmo de \_ codificação DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="e2c0a-103">DOT11\_CIPHER\_ALGORITHM enumeration</span></span>

<span data-ttu-id="e2c0a-104">O tipo enumerado do **\_ \_ algoritmo DOT11 Cipher** define um algoritmo de codificação para criptografia e descriptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-104">The **DOT11\_CIPHER\_ALGORITHM** enumerated type defines a cipher algorithm for data encryption and decryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c0a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2c0a-105">Syntax</span></span>


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="e2c0a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e2c0a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e2c0a-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11 \_ Cipher \_ algo \_ None**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11\_CIPHER\_ALGO\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-108">Especifica que nenhum algoritmo de codificação está habilitado ou com suporte.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-108">Specifies that no cipher algorithm is enabled or supported.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11 \_ Cipher \_ algo \_ WEP40**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11\_CIPHER\_ALGO\_WEP40**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-110">Especifica um algoritmo WEP (Wired Equivalent Privacy), que é o algoritmo baseado em RC4 que é especificado no padrão 802.11-1999.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-110">Specifies a Wired Equivalent Privacy (WEP) algorithm, which is the RC4-based algorithm that is specified in the 802.11-1999 standard.</span></span> <span data-ttu-id="e2c0a-111">Este enumerador especifica o algoritmo de criptografia WEP com uma chave de codificação de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-111">This enumerator specifies the WEP cipher algorithm with a 40-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_ \_ Algo TKIP de codificação DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11\_CIPHER\_ALGO\_TKIP**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-113">Especifica um algoritmo TKIP (Temporal Key Integrity Protocol), que é o conjunto de codificação baseado em RC4, baseado nos algoritmos definidos na especificação WPA e no padrão IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-113">Specifies a Temporal Key Integrity Protocol (TKIP) algorithm, which is the RC4-based cipher suite that is based on the algorithms that are defined in the WPA specification and IEEE 802.11i-2004 standard.</span></span> <span data-ttu-id="e2c0a-114">Essa codificação também usa o algoritmo de código de integridade de Michael Message (MIC) para a proteção de falsificação.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-114">This cipher also uses the Michael Message Integrity Code (MIC) algorithm for forgery protection.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11 \_ Cipher \_ algo \_ CCMP**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11\_CIPHER\_ALGO\_CCMP**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-116">Especifica um algoritmo AES-CCMP, conforme especificado no padrão IEEE 802.11 i-2004 e RFC 3610.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-116">Specifies an AES-CCMP algorithm, as specified in the IEEE 802.11i-2004 standard and RFC 3610.</span></span> <span data-ttu-id="e2c0a-117">O criptografia AES (AES) é o algoritmo de criptografia definido no FIPS PUB 197.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-117">Advanced Encryption Standard (AES) is the encryption algorithm defined in FIPS PUB 197.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11 \_ Cipher \_ algo \_ WEP104**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11\_CIPHER\_ALGO\_WEP104**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-119">Especifica um algoritmo de criptografia WEP com uma chave de codificação de 104 bits.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-119">Specifies a WEP cipher algorithm with a 104-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**\_Grupo de \_ uso de WPA de algo DOT11 Cipher \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11\_CIPHER\_ALGO\_WPA\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-121">Especifica um acesso protegido de Wi-Fi (WPA) usando o pacote de codificação de chave de grupo.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-121">Specifies a Wi-Fi Protected Access (WPA) Use Group Key cipher suite.</span></span> <span data-ttu-id="e2c0a-122">Para obter mais informações sobre o uso do conjunto de codificação de chave de grupo, consulte a cláusula 7.3.2.25.1 do padrão IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-122">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**\_Grupo de \_ uso de RSN de algo \_ \_ de DOT11 Cipher \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11\_CIPHER\_ALGO\_RSN\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-124">Especifica uma rede de segurança robusta (RSN) usando o pacote de codificação de chave de grupo.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-124">Specifies a Robust Security Network (RSN) Use Group Key cipher suite.</span></span> <span data-ttu-id="e2c0a-125">Para obter mais informações sobre o uso do conjunto de codificação de chave de grupo, consulte a cláusula 7.3.2.25.1 do padrão IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-125">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**\_ \_ Algo WEP de codificação DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11\_CIPHER\_ALGO\_WEP**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-127">Especifica um algoritmo de criptografia WEP com uma chave de codificação de qualquer comprimento.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-127">Specifies a WEP cipher algorithm with a cipher key of any length.</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**\_Início de IHV de codificação DOT11 \_ algo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11\_CIPHER\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-129">Especifica o início do intervalo que é usado para definir algoritmos de codificação proprietários que são desenvolvidos por um fornecedor de hardware independente (IHV).</span><span class="sxs-lookup"><span data-stu-id="e2c0a-129">Specifies the start of the range that is used to define proprietary cipher algorithms that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="e2c0a-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**\_Fim de IHV de codificação DOT11 \_ algo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11\_CIPHER\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="e2c0a-131">Especifica o final do intervalo que é usado para definir algoritmos de codificação proprietários que são desenvolvidos por um IHV.</span><span class="sxs-lookup"><span data-stu-id="e2c0a-131">Specifies the end of the range that is used to define proprietary cipher algorithms that are developed by an IHV.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2c0a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2c0a-132">Requirements</span></span>



| <span data-ttu-id="e2c0a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2c0a-133">Requirement</span></span> | <span data-ttu-id="e2c0a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e2c0a-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c0a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2c0a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c0a-136">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="e2c0a-136">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e2c0a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2c0a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c0a-138">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2c0a-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="e2c0a-139">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e2c0a-139">Redistributable</span></span><br/>          | <span data-ttu-id="e2c0a-140">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="e2c0a-140">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="e2c0a-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2c0a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2c0a-142"><dt>Wlantypes. h (incluir Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2c0a-142"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2c0a-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2c0a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c0a-144">**Par de codificação de DOT11 \_ auth \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-144">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="e2c0a-145">**rede de WLAN \_ disponível \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-145">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="e2c0a-146">**\_atributos de segurança de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="e2c0a-146">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




