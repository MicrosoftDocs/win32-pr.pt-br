---
description: Retorna uma coleção de OIDs que representa as políticas de certificado usadas para criar o objeto de cadeia.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: Método CertificateStatus. CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753928"
---
# <a name="certificatestatuscertificatepolicies-method"></a><span data-ttu-id="2f715-103">Método CertificateStatus. CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="2f715-103">CertificateStatus.CertificatePolicies method</span></span>

<span data-ttu-id="2f715-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2f715-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2f715-105">Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2f715-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2f715-106">O método **CertificatePolicies** retorna uma coleção de [**OIDs**](oids.md) que representa as políticas de certificado usadas para criar o objeto de [**cadeia**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="2f715-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f715-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f715-107">Syntax</span></span>


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="2f715-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f715-108">Parameters</span></span>

<span data-ttu-id="2f715-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2f715-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f715-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f715-110">Return value</span></span>

<span data-ttu-id="2f715-111">Uma coleção de [**OIDs**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="2f715-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="2f715-112">Cada objeto de [**OID**](oid.md) na coleção representa um OID de política de certificado.</span><span class="sxs-lookup"><span data-stu-id="2f715-112">Each [**OID**](oid.md) object in the collection represents a certificate policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f715-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f715-113">Remarks</span></span>

<span data-ttu-id="2f715-114">Adicione OIDs de política de certificado à coleção para especificar as políticas de certificado que devem ser usadas para criar a cadeia de certificados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="2f715-114">Add certificate policy OIDs to the collection to specify the certificate policies that should be used to build the certificate trust chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f715-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f715-115">Requirements</span></span>



| <span data-ttu-id="2f715-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f715-116">Requirement</span></span> | <span data-ttu-id="2f715-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2f715-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f715-118">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2f715-118">End of client support</span></span><br/> | <span data-ttu-id="2f715-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f715-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2f715-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2f715-120">End of server support</span></span><br/> | <span data-ttu-id="2f715-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f715-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2f715-122">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2f715-122">Redistributable</span></span><br/>       | <span data-ttu-id="2f715-123">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f715-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f715-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2f715-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2f715-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f715-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
