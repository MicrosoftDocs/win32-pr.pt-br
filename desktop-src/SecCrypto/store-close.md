---
description: Fecha um repositório de certificados aberto.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Método Store. Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756850"
---
# <a name="storeclose-method"></a><span data-ttu-id="86593-103">Método Store. Close</span><span class="sxs-lookup"><span data-stu-id="86593-103">Store.Close method</span></span>

<span data-ttu-id="86593-104">\[O método **Close** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="86593-104">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="86593-105">Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="86593-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="86593-106">O método **Close** fecha um [*repositório de certificados*](../secgloss/c-gly.md)aberto.</span><span class="sxs-lookup"><span data-stu-id="86593-106">The **Close** method closes an open [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="86593-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86593-107">Syntax</span></span>


```VB
Store.Close()
```



## <a name="parameters"></a><span data-ttu-id="86593-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86593-108">Parameters</span></span>

<span data-ttu-id="86593-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="86593-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86593-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86593-110">Return value</span></span>

<span data-ttu-id="86593-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="86593-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86593-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="86593-112">Remarks</span></span>

<span data-ttu-id="86593-113">Depois que o método **Close** é chamado, o objeto [**Store**](store.md) é destruído.</span><span class="sxs-lookup"><span data-stu-id="86593-113">After the **Close** method is called, the [**Store**](store.md) object is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="86593-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86593-114">Requirements</span></span>



| <span data-ttu-id="86593-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="86593-115">Requirement</span></span> | <span data-ttu-id="86593-116">Valor</span><span class="sxs-lookup"><span data-stu-id="86593-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86593-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="86593-117">Redistributable</span></span><br/> | <span data-ttu-id="86593-118">CAPICOM 2,1 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="86593-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="86593-119">DLL</span><span class="sxs-lookup"><span data-stu-id="86593-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="86593-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86593-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86593-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="86593-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86593-122">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="86593-122">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="86593-123">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="86593-123">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="86593-124">**Aberto**</span><span class="sxs-lookup"><span data-stu-id="86593-124">**Open**</span></span>](store-open.md)
</dt> </dl>

 

 
