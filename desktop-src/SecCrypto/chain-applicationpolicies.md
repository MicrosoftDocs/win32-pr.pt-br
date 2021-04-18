---
description: Retorna uma coleção de OIDs que representa os OIDs de política de aplicativo válidos para a cadeia.
ms.assetid: 4e4a7dce-5004-4b80-b132-3cdc0c048cde
title: 'Método IChain2:: ApplicationPolicies'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ApplicationPolicies
- IChain2.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a90eb7a493bfe81f5c4a38f773b0307380002b6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788111"
---
# <a name="ichain2applicationpolicies-method"></a><span data-ttu-id="a6dc7-103">Método IChain2:: ApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="a6dc7-103">IChain2::ApplicationPolicies method</span></span>

<span data-ttu-id="a6dc7-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a6dc7-105">Em vez disso, use a [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a6dc7-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a6dc7-106">O método **ApplicationPolicies** retorna uma coleção de [**OIDs**](oids.md) que representa os OIDs de política de aplicativo válidos para a cadeia.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span>

<span data-ttu-id="a6dc7-107">Esse método é introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6dc7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6dc7-108">Syntax</span></span>


```VB
Chain.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="a6dc7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6dc7-109">Parameters</span></span>

<span data-ttu-id="a6dc7-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a6dc7-110">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6dc7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6dc7-111">Requirements</span></span>



| <span data-ttu-id="a6dc7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6dc7-112">Requirement</span></span> | <span data-ttu-id="a6dc7-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a6dc7-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6dc7-114">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a6dc7-114">End of client support</span></span><br/> | <span data-ttu-id="a6dc7-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a6dc7-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a6dc7-116">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a6dc7-116">End of server support</span></span><br/> | <span data-ttu-id="a6dc7-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a6dc7-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a6dc7-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a6dc7-118">Redistributable</span></span><br/>       | <span data-ttu-id="a6dc7-119">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a6dc7-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a6dc7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a6dc7-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a6dc7-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6dc7-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
