---
description: Recupera o nome do repositório de certificados que este objeto representa.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Propriedade Store.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751513"
---
# <a name="storename-property"></a><span data-ttu-id="6b7e1-103">Propriedade Store.Name</span><span class="sxs-lookup"><span data-stu-id="6b7e1-103">Store.Name property</span></span>

<span data-ttu-id="6b7e1-104">\[A propriedade [**Name**](store-location.md) está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6b7e1-104">\[The [**Name**](store-location.md) property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6b7e1-105">Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="6b7e1-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6b7e1-106">A propriedade [**Name**](store-location.md) recupera o nome do repositório de certificados que este objeto representa.</span><span class="sxs-lookup"><span data-stu-id="6b7e1-106">The [**Name**](store-location.md) property retrieves the name of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b7e1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b7e1-107">Syntax</span></span>


```VB
Store.Name As String
```



## <a name="property-value"></a><span data-ttu-id="6b7e1-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6b7e1-108">Property value</span></span>

<span data-ttu-id="6b7e1-109">O valor da **cadeia de caracteres** que representa o nome do repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="6b7e1-109">The **String** value that represents the name of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b7e1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b7e1-110">Remarks</span></span>

<span data-ttu-id="6b7e1-111">Exemplos de nomes de repositório de certificados incluem My e root.</span><span class="sxs-lookup"><span data-stu-id="6b7e1-111">Examples of certificate store names include My and Root.</span></span>

<span data-ttu-id="6b7e1-112">O valor da propriedade [**Name**](store-location.md) é o mesmo que o valor fornecido para o parâmetro *StoreName* do método [**Open**](store-open.md) quando o armazenamento foi aberto.</span><span class="sxs-lookup"><span data-stu-id="6b7e1-112">The value of the [**Name**](store-location.md) property is the same as the value supplied for the *StoreName* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7e1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b7e1-113">Requirements</span></span>



| <span data-ttu-id="6b7e1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b7e1-114">Requirement</span></span> | <span data-ttu-id="6b7e1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6b7e1-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7e1-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="6b7e1-116">Redistributable</span></span><br/> | <span data-ttu-id="6b7e1-117">CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b7e1-117">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6b7e1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6b7e1-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="6b7e1-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b7e1-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b7e1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b7e1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7e1-121">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="6b7e1-121">**Store**</span></span>](store.md)
</dt> </dl>

 

 
