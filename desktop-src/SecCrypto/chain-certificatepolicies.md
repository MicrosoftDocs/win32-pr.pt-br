---
description: Retorna uma coleção de OIDs que representa os OIDs de política de certificado válidos para a cadeia.
ms.assetid: 18200003-f4f1-4cf3-af9a-bc223151ff68
title: 'Método IChain2:: CertificatePolicies'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.CertificatePolicies
- IChain2.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e37abce9ea1aec5eb8adaf1d8eceeb3fac284fa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758014"
---
# <a name="ichain2certificatepolicies-method"></a><span data-ttu-id="7f213-103">Método IChain2:: CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="7f213-103">IChain2::CertificatePolicies method</span></span>

<span data-ttu-id="7f213-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7f213-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7f213-105">Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="7f213-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="7f213-106">O método **CertificatePolicies** retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de certificado válidos para a cadeia.</span><span class="sxs-lookup"><span data-stu-id="7f213-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f213-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f213-107">Syntax</span></span>


```VB
Chain.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="7f213-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f213-108">Parameters</span></span>

<span data-ttu-id="7f213-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7f213-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f213-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f213-110">Requirements</span></span>



| <span data-ttu-id="7f213-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f213-111">Requirement</span></span> | <span data-ttu-id="7f213-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7f213-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f213-113">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7f213-113">End of client support</span></span><br/> | <span data-ttu-id="7f213-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f213-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7f213-115">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7f213-115">End of server support</span></span><br/> | <span data-ttu-id="7f213-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f213-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7f213-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7f213-117">Redistributable</span></span><br/>       | <span data-ttu-id="7f213-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f213-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7f213-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7f213-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7f213-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f213-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
