---
description: Remove um objeto de certificado de uma coleção de destinatários.
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: Método Recipients. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767825"
---
# <a name="recipientsremove-method"></a><span data-ttu-id="2f7d1-103">Método Recipients. Remove</span><span class="sxs-lookup"><span data-stu-id="2f7d1-103">Recipients.Remove method</span></span>

<span data-ttu-id="2f7d1-104">\[O método **Remove** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2f7d1-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f7d1-105">Em vez disso, use a [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2f7d1-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2f7d1-106">O método **Remove** remove um objeto de [**certificado**](certificate.md) de uma coleção de [**destinatários**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="2f7d1-106">The **Remove** method removes a [**Certificate**](certificate.md) object from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7d1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f7d1-107">Syntax</span></span>


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="2f7d1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f7d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7d1-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2f7d1-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7d1-110">Índice do objeto de [**certificado**](certificate.md) a ser removido da coleção.</span><span class="sxs-lookup"><span data-stu-id="2f7d1-110">Index of the [**Certificate**](certificate.md) object to be removed from the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7d1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f7d1-111">Return value</span></span>

<span data-ttu-id="2f7d1-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2f7d1-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f7d1-113">Requirements</span></span>



| <span data-ttu-id="2f7d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7d1-114">Requirement</span></span> | <span data-ttu-id="2f7d1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2f7d1-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7d1-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2f7d1-116">Redistributable</span></span><br/> | <span data-ttu-id="2f7d1-117">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f7d1-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f7d1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="2f7d1-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="2f7d1-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f7d1-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f7d1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f7d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7d1-121">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="2f7d1-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="2f7d1-122">**Destinatários**</span><span class="sxs-lookup"><span data-stu-id="2f7d1-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
