---
description: Contém uma chave de rede ou frase secreta.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Elemento keymaterial (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169709"
---
# <a name="keymaterial-sharedkey-element"></a><span data-ttu-id="a22d4-103">Elemento keymaterial (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="a22d4-103">keyMaterial (sharedKey) Element</span></span>

<span data-ttu-id="a22d4-104">O elemento keymaterial (sharedKey) contém uma chave de rede ou frase secreta.</span><span class="sxs-lookup"><span data-stu-id="a22d4-104">The keyMaterial (sharedKey) element contains a network key or passphrase.</span></span> <span data-ttu-id="a22d4-105">Se o elemento [**protegido**](wlan-profileschema-protected-sharedkey-element.md) tiver um valor de true, esse material da chave será criptografado; caso contrário, o material da chave será descriptografado.</span><span class="sxs-lookup"><span data-stu-id="a22d4-105">If the [**protected**](wlan-profileschema-protected-sharedkey-element.md) element has a value of TRUE, then this key material is encrypted; otherwise, the key material is unencrypted.</span></span> <span data-ttu-id="a22d4-106">O material de chave criptografado é expresso em formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="a22d4-106">Encrypted key material is expressed in hexadecimal form.</span></span>

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

<span data-ttu-id="a22d4-107">O elemento é definido pelo elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a22d4-107">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a22d4-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="a22d4-108">Remarks</span></span>

<span data-ttu-id="a22d4-109">O intervalo de valores válidos para o elemento keymaterial varia de acordo com o tipo de autenticação e criptografia usado, conforme especificado pelos elementos de [**autenticação**](wlan-profileschema-authentication-authencryption-element.md) e [**criptografia**](wlan-profileschema-encryption-authencryption-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a22d4-109">The range of valid values for the keyMaterial element varies by the type of authentication and encryption used, as specified by the [**authentication**](wlan-profileschema-authentication-authencryption-element.md) and [**encryption**](wlan-profileschema-encryption-authencryption-element.md) elements.</span></span> <span data-ttu-id="a22d4-110">Ele também varia por [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md).</span><span class="sxs-lookup"><span data-stu-id="a22d4-110">It also varies by [**keyType**](wlan-profileschema-keytype-sharedkey-element.md).</span></span>

<span data-ttu-id="a22d4-111">A tabela a seguir mostra valores de **keymaterial** válidos para alguns pares de autenticação e criptografia.</span><span class="sxs-lookup"><span data-stu-id="a22d4-111">The following table shows valid **keyMaterial** values for some authentication and encryption pairs.</span></span>



| <span data-ttu-id="a22d4-112">valor de [**autenticação**](wlan-profileschema-authentication-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="a22d4-112">[**authentication**](wlan-profileschema-authentication-authencryption-element.md) value</span></span> | <span data-ttu-id="a22d4-113">valor de [**criptografia**](wlan-profileschema-encryption-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="a22d4-113">[**encryption**](wlan-profileschema-encryption-authencryption-element.md) value</span></span> | <span data-ttu-id="a22d4-114">valor [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md)</span><span class="sxs-lookup"><span data-stu-id="a22d4-114">[**keyType**](wlan-profileschema-keytype-sharedkey-element.md) value</span></span> | <span data-ttu-id="a22d4-115">Valores de **Keymaterial** válidos</span><span class="sxs-lookup"><span data-stu-id="a22d4-115">Valid **keyMaterial** values</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a22d4-116">aberto ou compartilhado</span><span class="sxs-lookup"><span data-stu-id="a22d4-116">open or shared</span></span>                                                                           | <span data-ttu-id="a22d4-117">WEP</span><span class="sxs-lookup"><span data-stu-id="a22d4-117">WEP</span></span>                                                                              | <span data-ttu-id="a22d4-118">networkKey</span><span class="sxs-lookup"><span data-stu-id="a22d4-118">networkKey</span></span>                                                            | <span data-ttu-id="a22d4-119">Esse elemento contém uma chave WEP de 5 ou 13 caracteres ANSI, ou de 10 ou 26 caracteres hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="a22d4-119">This element contains a WEP key of 5 or 13 ANSI characters, or of 10 or 26 hexadecimal characters.</span></span>                                                                                             |
| <span data-ttu-id="a22d4-120">WPAPSK ou WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="a22d4-120">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="a22d4-121">TKIP ou AES</span><span class="sxs-lookup"><span data-stu-id="a22d4-121">TKIP or AES</span></span>                                                                      | <span data-ttu-id="a22d4-122">Senha</span><span class="sxs-lookup"><span data-stu-id="a22d4-122">passPhrase</span></span>                                                            | <span data-ttu-id="a22d4-123">Esse elemento contém uma frase secreta de 8 a 63 caracteres ASCII, ou seja, de 8 a 63 caracteres ANSI no intervalo de 32 a 126.</span><span class="sxs-lookup"><span data-stu-id="a22d4-123">This element contains a passphrase of 8 to 63 ASCII characters, that is, 8 to 63 ANSI characters in the range of 32 to 126.</span></span> <span data-ttu-id="a22d4-124">Os valores de chave devem estar em conformidade com os requisitos especificados pelo 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="a22d4-124">Key values must comply with the requirements specified by 802.11i.</span></span> |
| <span data-ttu-id="a22d4-125">WPAPSK ou WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="a22d4-125">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="a22d4-126">TKIP ou AES</span><span class="sxs-lookup"><span data-stu-id="a22d4-126">TKIP or AES</span></span>                                                                      | <span data-ttu-id="a22d4-127">networkKey</span><span class="sxs-lookup"><span data-stu-id="a22d4-127">networkKey</span></span>                                                            | <span data-ttu-id="a22d4-128">Esse elemento contém uma chave de 64 caracteres hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="a22d4-128">This element contains a key of 64 hexadecimal characters.</span></span>                                                                                                                                      |



 

<span data-ttu-id="a22d4-129">Caracteres Unicode podem ser inseridos onde os caracteres ANSI ou ASCII são especificados acima.</span><span class="sxs-lookup"><span data-stu-id="a22d4-129">Unicode characters may be entered where ANSI or ASCII characters are specified above.</span></span> <span data-ttu-id="a22d4-130">No entanto, se os caracteres Unicode fornecidos não puderem ser mapeados para caracteres ANSI ou ASCII, o material de chave fornecido será rejeitado.</span><span class="sxs-lookup"><span data-stu-id="a22d4-130">However, if the supplied Unicode characters cannot be mapped to ANSI or ASCII characters, then the supplied key material is rejected.</span></span>

<span data-ttu-id="a22d4-131">O material da chave retornado pelo [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) é sempre criptografado.</span><span class="sxs-lookup"><span data-stu-id="a22d4-131">Key material returned by [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) is always encrypted.</span></span> <span data-ttu-id="a22d4-132">Além disso, se o material de chave não criptografado for passado para [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), o material da chave será criptografado automaticamente antes de ser armazenado no repositório de perfis.</span><span class="sxs-lookup"><span data-stu-id="a22d4-132">Also, if unencrypted key material is passed to [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), the key material is automatically encrypted before it is stored in the profile store.</span></span>

<span data-ttu-id="a22d4-133">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** O material da chave nunca é criptografado.</span><span class="sxs-lookup"><span data-stu-id="a22d4-133">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The key material is never encrypted.</span></span>

<span data-ttu-id="a22d4-134">Se o processo for executado no contexto da conta LocalSystem, você poderá descriptografar o material da chave chamando [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="a22d4-134">If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span>

## <a name="examples"></a><span data-ttu-id="a22d4-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a22d4-135">Examples</span></span>

<span data-ttu-id="a22d4-136">Para exibir perfis de exemplo que usam o elemento **keymaterial** , consulte exemplo de [perfil sem difusão](non-broadcast-profile-sample.md), [exemplo de perfil WPA-Pessoal](wpa-personal-profile-sample.md)e [exemplo de perfil WPA2-Pessoal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a22d4-136">To view sample profiles that use the **keyMaterial** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a22d4-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a22d4-137">Requirements</span></span>



| <span data-ttu-id="a22d4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22d4-138">Requirement</span></span> | <span data-ttu-id="a22d4-139">Valor</span><span class="sxs-lookup"><span data-stu-id="a22d4-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a22d4-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a22d4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a22d4-141">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="a22d4-141">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a22d4-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a22d4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a22d4-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a22d4-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a22d4-144">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a22d4-144">Redistributable</span></span><br/>          | <span data-ttu-id="a22d4-145">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="a22d4-145">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a22d4-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="a22d4-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="a22d4-147">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a22d4-147">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a22d4-148">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="a22d4-148">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="a22d4-149">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a22d4-149">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a22d4-150">**sharedKey (segurança)**</span><span class="sxs-lookup"><span data-stu-id="a22d4-150">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
