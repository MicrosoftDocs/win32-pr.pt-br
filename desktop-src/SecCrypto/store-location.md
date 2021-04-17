---
description: Recupera o local do repositório de certificados que este objeto representa.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Propriedade Store. Location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752739"
---
# <a name="storelocation-property"></a><span data-ttu-id="4ca9c-103">Propriedade Store. Location</span><span class="sxs-lookup"><span data-stu-id="4ca9c-103">Store.Location property</span></span>

<span data-ttu-id="4ca9c-104">\[A propriedade **Location** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4ca9c-104">\[The **Location** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4ca9c-105">Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4ca9c-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4ca9c-106">A propriedade **Location** recupera o local do repositório de certificados que este objeto representa.</span><span class="sxs-lookup"><span data-stu-id="4ca9c-106">The **Location** property retrieves the location of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca9c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ca9c-107">Syntax</span></span>


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="4ca9c-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4ca9c-108">Property value</span></span>

<span data-ttu-id="4ca9c-109">O valor do [**\_ \_ local do armazenamento CAPICOM**](capicom-store-location.md) que representa o local do repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="4ca9c-109">The [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) value that represents the location of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ca9c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ca9c-110">Remarks</span></span>

<span data-ttu-id="4ca9c-111">O valor da propriedade **Location** é o mesmo que o valor fornecido para o parâmetro *StoreLocation* do método [**Open**](store-open.md) quando o armazenamento foi aberto.</span><span class="sxs-lookup"><span data-stu-id="4ca9c-111">The value of the **Location** property is the same as the value supplied for the *StoreLocation* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ca9c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca9c-112">Requirements</span></span>



| <span data-ttu-id="4ca9c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca9c-113">Requirement</span></span> | <span data-ttu-id="4ca9c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca9c-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca9c-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4ca9c-115">Redistributable</span></span><br/> | <span data-ttu-id="4ca9c-116">CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ca9c-116">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4ca9c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="4ca9c-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="4ca9c-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ca9c-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ca9c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ca9c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ca9c-120">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="4ca9c-120">**Store**</span></span>](store.md)
</dt> </dl>

 

 
