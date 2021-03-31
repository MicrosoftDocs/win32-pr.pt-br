---
description: Indica se o modo FIPS (Federal Information Processing Standards) está habilitado.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Elemento FIPSmode (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647350"
---
# <a name="fipsmode-authencryption-element"></a><span data-ttu-id="a00a7-103">Elemento FIPSmode (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="a00a7-103">FIPSMode (authEncryption) Element</span></span>

<span data-ttu-id="a00a7-104">O elemento **fipsmode** (authEncryption) indica se o modo FIPS (Federal Information Processing Standards) está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a00a7-104">The **FIPSMode** (authEncryption) element indicates whether Federal Information Processing Standards (FIPS) mode is enabled.</span></span> <span data-ttu-id="a00a7-105">Quando uma conexão sem fio está operando no modo FIPS, o nível de segurança da conexão é compatível com o padrão FIPS 140-2.</span><span class="sxs-lookup"><span data-stu-id="a00a7-105">When a wireless connection is operating in FIPS mode, the security level of the connection complies with the FIPS 140-2 standard.</span></span> <span data-ttu-id="a00a7-106">Para obter mais informações sobre o FIPS, consulte a [Home Page do FIPS](https://www.itl.nist.gov/fipspubs/).</span><span class="sxs-lookup"><span data-stu-id="a00a7-106">For more information about FIPS, see the [FIPS Home Page](https://www.itl.nist.gov/fipspubs/).</span></span>

<span data-ttu-id="a00a7-107">Esse elemento é opcional.</span><span class="sxs-lookup"><span data-stu-id="a00a7-107">This element is optional.</span></span> <span data-ttu-id="a00a7-108">Se esse elemento não for especificado em um perfil, o modo FIPS não estará habilitado.</span><span class="sxs-lookup"><span data-stu-id="a00a7-108">If this element is not specified in a profile, then FIPS mode is not enabled.</span></span>

<span data-ttu-id="a00a7-109">O **fipsmode** pode ser definido como true somente quando as seguintes condições são atendidas:</span><span class="sxs-lookup"><span data-stu-id="a00a7-109">**FIPSMode** can be set to TRUE only when the following conditions are met:</span></span>

-   <span data-ttu-id="a00a7-110">O elemento [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) tem um valor de `ESS` (ou seja, a conexão é uma conexão de infraestrutura).</span><span class="sxs-lookup"><span data-stu-id="a00a7-110">The [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) element has a value of `ESS` (that is, the connection is an infrastructure connection).</span></span>
-   <span data-ttu-id="a00a7-111">O elemento de [**autenticação**](wlan-profileschema-authentication-authencryption-element.md) tem um valor de `WPA2` ou `WPA2PSK` .</span><span class="sxs-lookup"><span data-stu-id="a00a7-111">The [**authentication**](wlan-profileschema-authentication-authencryption-element.md) element has a value of `WPA2` or `WPA2PSK`.</span></span>
-   <span data-ttu-id="a00a7-112">O elemento [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) tem um valor de `AES` .</span><span class="sxs-lookup"><span data-stu-id="a00a7-112">The [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of `AES`.</span></span>

<span data-ttu-id="a00a7-113">Ao contrário da maioria dos elementos no esquema de perfil de WLAN \_ , esse elemento está no `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.</span><span class="sxs-lookup"><span data-stu-id="a00a7-113">Unlike most elements in the WLAN\_profile schema, this element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.</span></span>

<span data-ttu-id="a00a7-114">O valor do elemento **fipsmode** será ignorado se o driver de Miniport da interface sem fio não oferecer suporte ao modo FIPS.</span><span class="sxs-lookup"><span data-stu-id="a00a7-114">The value of the **FIPSMode** element is ignored if the miniport driver for the wireless interface does not support FIPS mode.</span></span>

<span data-ttu-id="a00a7-115">**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.</span><span class="sxs-lookup"><span data-stu-id="a00a7-115">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span> <span data-ttu-id="a00a7-116">Se **fipsmode** estiver presente em um perfil, o elemento será ignorado.</span><span class="sxs-lookup"><span data-stu-id="a00a7-116">If **FIPSMode** is present in a profile, the element is ignored.</span></span>

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

<span data-ttu-id="a00a7-117">O elemento é definido pelo elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a00a7-117">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a00a7-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a00a7-118">Remarks</span></span>

<span data-ttu-id="a00a7-119">Esse parâmetro pode ser definido na linha de comando usando o comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="a00a7-119">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="a00a7-120">Para obter mais informações, consulte [comandos netsh para rede local sem fio (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="a00a7-120">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="examples"></a><span data-ttu-id="a00a7-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a00a7-121">Examples</span></span>

<span data-ttu-id="a00a7-122">Para exibir um perfil de exemplo que usa o elemento **fipsmode** , consulte [exemplo de perfil FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a00a7-122">To view a sample profile that uses the **FIPSMode** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a00a7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a00a7-123">Requirements</span></span>



| <span data-ttu-id="a00a7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a00a7-124">Requirement</span></span> | <span data-ttu-id="a00a7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a00a7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a00a7-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a00a7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a00a7-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a00a7-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a00a7-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a00a7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a00a7-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a00a7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a00a7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a00a7-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a00a7-131">**Contexto de definição do elemento no esquema**</span><span class="sxs-lookup"><span data-stu-id="a00a7-131">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a00a7-132">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="a00a7-132">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="a00a7-133">**Possível elemento pai imediato na instância de esquema**</span><span class="sxs-lookup"><span data-stu-id="a00a7-133">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a00a7-134">**authEncryption (segurança)**</span><span class="sxs-lookup"><span data-stu-id="a00a7-134">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
