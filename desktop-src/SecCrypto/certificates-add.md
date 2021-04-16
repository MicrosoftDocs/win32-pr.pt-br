---
description: Adiciona um objeto de certificado à coleção.
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: 'Método ICertificates2:: Add'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754121"
---
# <a name="icertificates2add-method"></a><span data-ttu-id="45b38-103">Método ICertificates2:: Add</span><span class="sxs-lookup"><span data-stu-id="45b38-103">ICertificates2::Add method</span></span>

<span data-ttu-id="45b38-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="45b38-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="45b38-105">Em vez disso, use a [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="45b38-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="45b38-106">O método **Add** adiciona um objeto de [**certificado**](certificate.md) à coleção.</span><span class="sxs-lookup"><span data-stu-id="45b38-106">The **Add** method adds a [**Certificate**](certificate.md) object to the collection.</span></span> <span data-ttu-id="45b38-107">Esse método é introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="45b38-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b38-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45b38-108">Syntax</span></span>


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="45b38-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45b38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45b38-110">*Certificado* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="45b38-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45b38-111">O objeto de [**certificado**](certificate.md) a ser adicionado à coleção.</span><span class="sxs-lookup"><span data-stu-id="45b38-111">The [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45b38-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45b38-112">Return value</span></span>

<span data-ttu-id="45b38-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="45b38-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b38-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b38-114">Requirements</span></span>



| <span data-ttu-id="45b38-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b38-115">Requirement</span></span> | <span data-ttu-id="45b38-116">Valor</span><span class="sxs-lookup"><span data-stu-id="45b38-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45b38-117">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="45b38-117">End of client support</span></span><br/> | <span data-ttu-id="45b38-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45b38-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="45b38-119">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="45b38-119">End of server support</span></span><br/> | <span data-ttu-id="45b38-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45b38-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="45b38-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="45b38-121">Redistributable</span></span><br/>       | <span data-ttu-id="45b38-122">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="45b38-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="45b38-123">DLL</span><span class="sxs-lookup"><span data-stu-id="45b38-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="45b38-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b38-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
