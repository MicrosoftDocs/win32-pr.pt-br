---
description: Retorna uma coleção de OIDs que representa as políticas de aplicativo usadas para criar o objeto de cadeia.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: Método CertificateStatus. ApplicationPolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762022"
---
# <a name="certificatestatusapplicationpolicies-method"></a><span data-ttu-id="181fd-103">Método CertificateStatus. ApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="181fd-103">CertificateStatus.ApplicationPolicies method</span></span>

<span data-ttu-id="181fd-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="181fd-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="181fd-105">Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="181fd-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="181fd-106">O método **ApplicationPolicies** retorna uma coleção de [**OIDs**](oids.md) que representa as políticas de aplicativo usadas para criar o objeto de [**cadeia**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="181fd-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="181fd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="181fd-107">Syntax</span></span>


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="181fd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="181fd-108">Parameters</span></span>

<span data-ttu-id="181fd-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="181fd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="181fd-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="181fd-110">Return value</span></span>

<span data-ttu-id="181fd-111">Uma coleção de [**OIDs**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="181fd-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="181fd-112">Cada objeto de [**OID**](oid.md) na coleção representa um OID de política de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="181fd-112">Each [**OID**](oid.md) object in the collection represents an application policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="181fd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="181fd-113">Remarks</span></span>

<span data-ttu-id="181fd-114">Adicione OIDs de política de aplicativo à coleção para especificar as políticas de aplicativo que devem ser usadas para criar a cadeia de certificados confiáveis.</span><span class="sxs-lookup"><span data-stu-id="181fd-114">Add application policy OIDs to the collection to specify the application policies that should be used to build the certificate trust chain.</span></span> <span data-ttu-id="181fd-115">Se a coleção contiver pelo menos um objeto [**OID**](oid.md) , o objeto [**EKU**](eku.md) retornado pelo método [**CertificateStatus. EKU**](certificatestatus-eku.md) será ignorado.</span><span class="sxs-lookup"><span data-stu-id="181fd-115">If the collection contains at least one [**OID**](oid.md) object, the [**EKU**](eku.md) object returned by the [**CertificateStatus.EKU**](certificatestatus-eku.md) method is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="181fd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="181fd-116">Requirements</span></span>



| <span data-ttu-id="181fd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="181fd-117">Requirement</span></span> | <span data-ttu-id="181fd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="181fd-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="181fd-119">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="181fd-119">End of client support</span></span><br/> | <span data-ttu-id="181fd-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="181fd-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="181fd-121">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="181fd-121">End of server support</span></span><br/> | <span data-ttu-id="181fd-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="181fd-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="181fd-123">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="181fd-123">Redistributable</span></span><br/>       | <span data-ttu-id="181fd-124">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="181fd-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="181fd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="181fd-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="181fd-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="181fd-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
