---
description: Adiciona um objeto de certificado a uma coleção de destinatários.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Método Recipients. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769274"
---
# <a name="recipientsadd-method"></a><span data-ttu-id="cfd74-103">Método Recipients. Add</span><span class="sxs-lookup"><span data-stu-id="cfd74-103">Recipients.Add method</span></span>

<span data-ttu-id="cfd74-104">\[O método **Add** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="cfd74-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cfd74-105">Em vez disso, use a [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="cfd74-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="cfd74-106">O método **Add** adiciona um objeto de [**certificado**](certificate.md) a uma coleção de [**destinatários**](recipients.md) .</span><span class="sxs-lookup"><span data-stu-id="cfd74-106">The **Add** method adds a [**Certificate**](certificate.md) object to a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd74-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfd74-107">Syntax</span></span>


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="cfd74-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfd74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd74-109">*Certificado* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="cfd74-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfd74-110">Expressão que resolve para o objeto de [**certificado**](certificate.md) a ser adicionado à coleção.</span><span class="sxs-lookup"><span data-stu-id="cfd74-110">Expression that resolves to the [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd74-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfd74-111">Return value</span></span>

<span data-ttu-id="cfd74-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cfd74-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd74-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfd74-113">Requirements</span></span>



| <span data-ttu-id="cfd74-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfd74-114">Requirement</span></span> | <span data-ttu-id="cfd74-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cfd74-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd74-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="cfd74-116">Redistributable</span></span><br/> | <span data-ttu-id="cfd74-117">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="cfd74-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cfd74-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cfd74-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="cfd74-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfd74-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd74-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfd74-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd74-121">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="cfd74-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="cfd74-122">**Destinatários**</span><span class="sxs-lookup"><span data-stu-id="cfd74-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
