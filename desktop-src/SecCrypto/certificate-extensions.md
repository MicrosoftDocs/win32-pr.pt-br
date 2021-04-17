---
description: Retorna uma coleção das extensões associadas ao certificado.
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: 'Método ICertificate2:: Extensions'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cc96dee9c33bb3f76e1fb17acb2000f9740d1b5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755053"
---
# <a name="icertificate2extensions-method"></a><span data-ttu-id="88956-103">Método ICertificate2:: Extensions</span><span class="sxs-lookup"><span data-stu-id="88956-103">ICertificate2::Extensions method</span></span>

<span data-ttu-id="88956-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88956-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="88956-105">Em vez disso, use a [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="88956-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="88956-106">O método **Extensions** retorna uma coleção das extensões associadas ao certificado.</span><span class="sxs-lookup"><span data-stu-id="88956-106">The **Extensions** method returns a collection of the extensions associated with the certificate.</span></span> <span data-ttu-id="88956-107">Esse método é introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="88956-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="88956-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88956-108">Syntax</span></span>


```VB
Certificate.Extensions()
```



## <a name="parameters"></a><span data-ttu-id="88956-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88956-109">Parameters</span></span>

<span data-ttu-id="88956-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="88956-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88956-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88956-111">Return value</span></span>

<span data-ttu-id="88956-112">Um objeto de [**extensões**](extensions.md) que representa todas as extensões associadas ao certificado.</span><span class="sxs-lookup"><span data-stu-id="88956-112">An [**Extensions**](extensions.md) object that represents all of the extensions associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="88956-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88956-113">Requirements</span></span>



| <span data-ttu-id="88956-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="88956-114">Requirement</span></span> | <span data-ttu-id="88956-115">Valor</span><span class="sxs-lookup"><span data-stu-id="88956-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88956-116">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="88956-116">End of client support</span></span><br/> | <span data-ttu-id="88956-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88956-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="88956-118">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="88956-118">End of server support</span></span><br/> | <span data-ttu-id="88956-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88956-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="88956-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="88956-120">Redistributable</span></span><br/>       | <span data-ttu-id="88956-121">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="88956-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="88956-122">DLL</span><span class="sxs-lookup"><span data-stu-id="88956-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="88956-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88956-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
