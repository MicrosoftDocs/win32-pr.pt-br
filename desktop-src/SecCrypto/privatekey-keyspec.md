---
description: Recupera a especificação de chave.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: Propriedade PrivateKey. KeySpec
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757468"
---
# <a name="privatekeykeyspec-property"></a><span data-ttu-id="00016-103">Propriedade PrivateKey. KeySpec</span><span class="sxs-lookup"><span data-stu-id="00016-103">PrivateKey.KeySpec property</span></span>

<span data-ttu-id="00016-104">\[A propriedade **KeySpec** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="00016-104">\[The **KeySpec** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00016-105">Em vez disso, use a [**Propriedade X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="00016-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="00016-106">A propriedade **KeySpec** recupera a especificação da chave.</span><span class="sxs-lookup"><span data-stu-id="00016-106">The **KeySpec** property retrieves the key specification.</span></span>

## <a name="syntax"></a><span data-ttu-id="00016-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="00016-107">Syntax</span></span>


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a><span data-ttu-id="00016-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="00016-108">Property value</span></span>

<span data-ttu-id="00016-109">Um valor da enumeração [**de \_ \_ espec da chave de CAPICOM**](capicom-key-spec.md) que indica a especificação da chave.</span><span class="sxs-lookup"><span data-stu-id="00016-109">A value of the [**CAPICOM\_KEY\_SPEC**](capicom-key-spec.md) enumeration that indicates the key specification.</span></span> <span data-ttu-id="00016-110">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="00016-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="00016-111">Valor</span><span class="sxs-lookup"><span data-stu-id="00016-111">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="00016-112">Significado</span><span class="sxs-lookup"><span data-stu-id="00016-112">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <span data-ttu-id="00016-113"><dt>**chave de capicor \_ \_ spec Key \_ Exchange**</dt></span><span class="sxs-lookup"><span data-stu-id="00016-113"><dt>**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</dt></span></span> </dl> | <span data-ttu-id="00016-114">A chave pode ser usada para criptografia e assinatura.</span><span class="sxs-lookup"><span data-stu-id="00016-114">The key can be used for encryption and signing.</span></span><br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <span data-ttu-id="00016-115"><dt>**\_assinatura de \_ espec de chave de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="00016-115"><dt>**CAPICOM\_KEY\_SPEC\_SIGNATURE**</dt></span></span> </dl>       | <span data-ttu-id="00016-116">A chave só pode ser usada para assinatura.</span><span class="sxs-lookup"><span data-stu-id="00016-116">The key can be used only for signing.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="00016-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00016-117">Requirements</span></span>



| <span data-ttu-id="00016-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="00016-118">Requirement</span></span> | <span data-ttu-id="00016-119">Valor</span><span class="sxs-lookup"><span data-stu-id="00016-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00016-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="00016-120">Redistributable</span></span><br/> | <span data-ttu-id="00016-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="00016-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="00016-122">DLL</span><span class="sxs-lookup"><span data-stu-id="00016-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="00016-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00016-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00016-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="00016-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00016-125">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="00016-125">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
