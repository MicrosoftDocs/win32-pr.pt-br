---
description: Define ou recupera a opção de certificado do signatário.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Propriedade signatário. Options
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753392"
---
# <a name="signeroptions-property"></a><span data-ttu-id="6bc98-103">Propriedade signatário. Options</span><span class="sxs-lookup"><span data-stu-id="6bc98-103">Signer.Options property</span></span>

<span data-ttu-id="6bc98-104">\[A propriedade **Options** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6bc98-104">\[The **Options** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6bc98-105">Em vez disso, use a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="6bc98-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6bc98-106">A propriedade **Options** define ou recupera a opção de certificado do signatário.</span><span class="sxs-lookup"><span data-stu-id="6bc98-106">The **Options** property sets or retrieves the signer's certificate option.</span></span>

<span data-ttu-id="6bc98-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6bc98-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bc98-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6bc98-108">Syntax</span></span>


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a><span data-ttu-id="6bc98-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6bc98-109">Property value</span></span>

<span data-ttu-id="6bc98-110">Um valor do [**certificado CAPICOM \_ \_ inclui \_**](capicom-certificate-include-option.md) a enumeração de opção que especifica a opção de certificado do signatário.</span><span class="sxs-lookup"><span data-stu-id="6bc98-110">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies the signer's certificate option.</span></span> <span data-ttu-id="6bc98-111">O valor padrão é capicor certificado de caminhagem \_ \_ \_ \_ , exceto \_ raiz.</span><span class="sxs-lookup"><span data-stu-id="6bc98-111">The default value is CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT.</span></span> <span data-ttu-id="6bc98-112">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="6bc98-112">The following table shows the possible values.</span></span>



| <span data-ttu-id="6bc98-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6bc98-113">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="6bc98-114">Significado</span><span class="sxs-lookup"><span data-stu-id="6bc98-114">Meaning</span></span>                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="6bc98-115"><dt>**CAPICOM de certificado de caissor \_ \_ \_ \_ , exceto \_ raiz**</dt></span><span class="sxs-lookup"><span data-stu-id="6bc98-115"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="6bc98-116">Salva todos os certificados na cadeia com a exceção da entidade raiz.</span><span class="sxs-lookup"><span data-stu-id="6bc98-116">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="6bc98-117"><dt>**certificado CAPICOM \_ \_ incluir \_ \_ cadeia inteira**</dt></span><span class="sxs-lookup"><span data-stu-id="6bc98-117"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="6bc98-118">Salva a cadeia de certificados completa.</span><span class="sxs-lookup"><span data-stu-id="6bc98-118">Saves the complete certificate chain.</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="6bc98-119"><dt>**o certificado CAPICOM \_ \_ inclui \_ \_ somente entidade final \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6bc98-119"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="6bc98-120">Salva apenas o certificado de entidade final.</span><span class="sxs-lookup"><span data-stu-id="6bc98-120">Saves only the end entity certificate.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="6bc98-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bc98-121">Requirements</span></span>



| <span data-ttu-id="6bc98-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bc98-122">Requirement</span></span> | <span data-ttu-id="6bc98-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6bc98-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bc98-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6bc98-124">Redistributable</span></span><br/> | <span data-ttu-id="6bc98-125">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6bc98-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6bc98-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6bc98-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="6bc98-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bc98-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bc98-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bc98-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bc98-129">**Signatário**</span><span class="sxs-lookup"><span data-stu-id="6bc98-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
