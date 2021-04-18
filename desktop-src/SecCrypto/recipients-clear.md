---
description: Remove todos os objetos de certificado de uma coleção de destinatários.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Método Recipients. Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784142"
---
# <a name="recipientsclear-method"></a><span data-ttu-id="1533a-103">Método Recipients. Clear</span><span class="sxs-lookup"><span data-stu-id="1533a-103">Recipients.Clear method</span></span>

<span data-ttu-id="1533a-104">\[O método **Clear** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1533a-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1533a-105">Em vez disso, use a [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="1533a-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1533a-106">O método **Clear** remove todos os objetos de [**certificado**](certificate.md) de uma coleção de [**destinatários**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="1533a-106">The **Clear** method removes all [**Certificate**](certificate.md) objects from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1533a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1533a-107">Syntax</span></span>


```VB
Recipients.Clear()
```



## <a name="parameters"></a><span data-ttu-id="1533a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1533a-108">Parameters</span></span>

<span data-ttu-id="1533a-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1533a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1533a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1533a-110">Return value</span></span>

<span data-ttu-id="1533a-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1533a-111">This method does not return a value.</span></span> <span data-ttu-id="1533a-112">Um aplicativo que usa esse método deve conter código para manipular uma exceção gerada por esse método.</span><span class="sxs-lookup"><span data-stu-id="1533a-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1533a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1533a-113">Requirements</span></span>



| <span data-ttu-id="1533a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1533a-114">Requirement</span></span> | <span data-ttu-id="1533a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1533a-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1533a-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="1533a-116">Redistributable</span></span><br/> | <span data-ttu-id="1533a-117">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="1533a-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1533a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="1533a-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="1533a-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1533a-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1533a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1533a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1533a-121">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="1533a-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="1533a-122">**Destinatários**</span><span class="sxs-lookup"><span data-stu-id="1533a-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
