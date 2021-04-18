---
description: Remove um único objeto de certificado da coleção.
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: 'Método ICertificates2:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758017"
---
# <a name="icertificates2remove-method"></a><span data-ttu-id="f5e63-103">Método ICertificates2:: Remove</span><span class="sxs-lookup"><span data-stu-id="f5e63-103">ICertificates2::Remove method</span></span>

<span data-ttu-id="f5e63-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f5e63-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f5e63-105">Em vez disso, use a [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f5e63-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f5e63-106">O método **Remove** remove um único objeto de [**certificado**](certificate.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="f5e63-106">The **Remove** method removes a single [**Certificate**](certificate.md) object from the collection.</span></span> <span data-ttu-id="f5e63-107">Esse método foi introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f5e63-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e63-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5e63-108">Syntax</span></span>


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="f5e63-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5e63-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5e63-110">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f5e63-110">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5e63-111">Valor de índice do objeto de [**certificado**](certificate.md) a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f5e63-111">Index value for the [**Certificate**](certificate.md) object to be removed.</span></span> <span data-ttu-id="f5e63-112">Esse parâmetro pode ser um dos seguintes tipos possíveis.</span><span class="sxs-lookup"><span data-stu-id="f5e63-112">This parameter can be one of the following possible types.</span></span>



| <span data-ttu-id="f5e63-113">Type</span><span class="sxs-lookup"><span data-stu-id="f5e63-113">Type</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="f5e63-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f5e63-114">Meaning</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <span data-ttu-id="f5e63-115"><dt>\* \* \* \* Long \* \* \* \*</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5e63-115"><dt>\*\*\*\*Long\*\*\*\*</dt> <dt></dt></span></span> </dl>                                                | <span data-ttu-id="f5e63-116">O objeto de [**certificado**](certificate.md) no índice especificado na coleção é removido.</span><span class="sxs-lookup"><span data-stu-id="f5e63-116">The [**Certificate**](certificate.md) object at the specified index into the collection is removed.</span></span><br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="f5e63-117">\* \* \* \* <dt>Cadeia de caracteres \*</dt> \* \* \*<dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5e63-117"><dt>\*\*\*\*String\*\*\*\*</dt> <dt></dt></span></span> </dl>                                        | <span data-ttu-id="f5e63-118">O primeiro objeto de [**certificado**](certificate.md) na coleção que corresponde à impressão digital [*SHA-1*](../secgloss/s-gly.md) contido na cadeia de caracteres especificada é removido.</span><span class="sxs-lookup"><span data-stu-id="f5e63-118">The first [**Certificate**](certificate.md) object in the collection that matches the [*SHA-1*](../secgloss/s-gly.md) thumbprint contained in the specified string is removed.</span></span><br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <span data-ttu-id="f5e63-119"><dt>**[**Certificado**](certificate.md)**</dt> do <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f5e63-119"><dt>**[**Certificate**](certificate.md)**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="f5e63-120">O primeiro objeto de [**certificado**](certificate.md) na coleção que corresponde ao objeto de **certificado** especificado é removido.</span><span class="sxs-lookup"><span data-stu-id="f5e63-120">The first [**Certificate**](certificate.md) object in the collection that matches the specified **Certificate** object is removed.</span></span><br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5e63-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5e63-121">Return value</span></span>

<span data-ttu-id="f5e63-122">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f5e63-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5e63-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5e63-123">Requirements</span></span>



| <span data-ttu-id="f5e63-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e63-124">Requirement</span></span> | <span data-ttu-id="f5e63-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f5e63-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5e63-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="f5e63-126">End of client support</span></span><br/> | <span data-ttu-id="f5e63-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5e63-127">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f5e63-128">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f5e63-128">End of server support</span></span><br/> | <span data-ttu-id="f5e63-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5e63-129">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f5e63-130">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f5e63-130">Redistributable</span></span><br/>       | <span data-ttu-id="f5e63-131">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5e63-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f5e63-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f5e63-132">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f5e63-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5e63-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
