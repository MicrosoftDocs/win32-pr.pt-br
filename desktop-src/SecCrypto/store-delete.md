---
description: Exclui o repositório de certificados que é representado pelo objeto de armazenamento atual.
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Método Store. Delete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752125"
---
# <a name="storedelete-method"></a><span data-ttu-id="822df-103">Método Store. Delete</span><span class="sxs-lookup"><span data-stu-id="822df-103">Store.Delete method</span></span>

<span data-ttu-id="822df-104">\[O método **delete** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="822df-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="822df-105">Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="822df-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="822df-106">O método **delete** exclui o [*repositório de certificados*](../secgloss/c-gly.md) que é representado pelo objeto de [**armazenamento**](certificate.md) atual.</span><span class="sxs-lookup"><span data-stu-id="822df-106">The **Delete** method deletes the [*certificate store*](../secgloss/c-gly.md) that is represented by the current [**Store**](certificate.md) object.</span></span> <span data-ttu-id="822df-107">Esse método exclui somente os repositórios que não são do sistema.</span><span class="sxs-lookup"><span data-stu-id="822df-107">This method deletes only nonsystem stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="822df-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="822df-108">Syntax</span></span>


```VB
Store.Delete()
```



## <a name="parameters"></a><span data-ttu-id="822df-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="822df-109">Parameters</span></span>

<span data-ttu-id="822df-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="822df-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="822df-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="822df-111">Return value</span></span>

<span data-ttu-id="822df-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="822df-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="822df-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="822df-113">Remarks</span></span>

<span data-ttu-id="822df-114">Os repositórios a seguir são repositórios do sistema e não podem ser excluídos:</span><span class="sxs-lookup"><span data-stu-id="822df-114">The following stores are system stores and cannot be deleted:</span></span>

-   <span data-ttu-id="822df-115">Meu</span><span class="sxs-lookup"><span data-stu-id="822df-115">My</span></span>
-   <span data-ttu-id="822df-116">Root</span><span class="sxs-lookup"><span data-stu-id="822df-116">Root</span></span>
-   <span data-ttu-id="822df-117">Confiar</span><span class="sxs-lookup"><span data-stu-id="822df-117">Trust</span></span>
-   <span data-ttu-id="822df-118">AC</span><span class="sxs-lookup"><span data-stu-id="822df-118">CA</span></span>
-   <span data-ttu-id="822df-119">UserDS</span><span class="sxs-lookup"><span data-stu-id="822df-119">UserDS</span></span>
-   <span data-ttu-id="822df-120">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="822df-120">TrustedPublisher</span></span>
-   <span data-ttu-id="822df-121">Não permitido</span><span class="sxs-lookup"><span data-stu-id="822df-121">Disallowed</span></span>
-   <span data-ttu-id="822df-122">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="822df-122">AuthRoot</span></span>
-   <span data-ttu-id="822df-123">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="822df-123">TrustedPeople</span></span>

<span data-ttu-id="822df-124">O método **delete** retornará um erro se for chamado a partir de um script da Web.</span><span class="sxs-lookup"><span data-stu-id="822df-124">The **Delete** method returns an error if called from a web script.</span></span>

## <a name="requirements"></a><span data-ttu-id="822df-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="822df-125">Requirements</span></span>



| <span data-ttu-id="822df-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="822df-126">Requirement</span></span> | <span data-ttu-id="822df-127">Valor</span><span class="sxs-lookup"><span data-stu-id="822df-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="822df-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="822df-128">Redistributable</span></span><br/> | <span data-ttu-id="822df-129">CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="822df-129">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="822df-130">DLL</span><span class="sxs-lookup"><span data-stu-id="822df-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="822df-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="822df-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="822df-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="822df-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822df-133">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="822df-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="822df-134">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="822df-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
