---
description: Retorna um objeto BasicConstraints que representa a extensão de restrições básicas do certificado.
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: 'Método ICertificate2:: BasicConstraints'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b511781c29d313715e7714f185dbff7e4b38f86c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811802"
---
# <a name="icertificate2basicconstraints-method"></a><span data-ttu-id="6244c-103">Método ICertificate2:: BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="6244c-103">ICertificate2::BasicConstraints method</span></span>

<span data-ttu-id="6244c-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6244c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6244c-105">Em vez disso, use a [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6244c-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6244c-106">O método **BasicConstraints** retorna um objeto [**BasicConstraints**](basicconstraints.md) que representa a extensão de restrições básicas do certificado.</span><span class="sxs-lookup"><span data-stu-id="6244c-106">The **BasicConstraints** method returns a [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="6244c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6244c-107">Syntax</span></span>


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a><span data-ttu-id="6244c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6244c-108">Parameters</span></span>

<span data-ttu-id="6244c-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6244c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6244c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6244c-110">Return value</span></span>

<span data-ttu-id="6244c-111">O objeto [**BasicConstraints**](basicconstraints.md) que representa a extensão de restrições básicas do certificado.</span><span class="sxs-lookup"><span data-stu-id="6244c-111">The [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6244c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6244c-112">Requirements</span></span>



| <span data-ttu-id="6244c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6244c-113">Requirement</span></span> | <span data-ttu-id="6244c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="6244c-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6244c-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6244c-115">End of client support</span></span><br/> | <span data-ttu-id="6244c-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6244c-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6244c-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="6244c-117">End of server support</span></span><br/> | <span data-ttu-id="6244c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6244c-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6244c-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6244c-119">Redistributable</span></span><br/>       | <span data-ttu-id="6244c-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6244c-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6244c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6244c-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6244c-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6244c-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
