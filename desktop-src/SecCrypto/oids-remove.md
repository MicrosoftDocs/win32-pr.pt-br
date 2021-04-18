---
description: Remove o objeto OID especificado da coleção.
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: Método OIDs. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796372"
---
# <a name="oidsremove-method"></a><span data-ttu-id="549c7-103">Método OIDs. Remove</span><span class="sxs-lookup"><span data-stu-id="549c7-103">OIDs.Remove method</span></span>

<span data-ttu-id="549c7-104">\[O método **Remove** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="549c7-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="549c7-105">Em vez disso, use a [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="549c7-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="549c7-106">O método **Remove** remove o objeto [**OID**](oid.md) especificado da coleção.</span><span class="sxs-lookup"><span data-stu-id="549c7-106">The **Remove** method removes the specified [**OID**](oid.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="549c7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="549c7-107">Syntax</span></span>


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="549c7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="549c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="549c7-109">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="549c7-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="549c7-110">Índice do objeto de [**OID**](oid.md) a ser removido.</span><span class="sxs-lookup"><span data-stu-id="549c7-110">Index of the [**OID**](oid.md) object to be removed.</span></span> <span data-ttu-id="549c7-111">Pode ser um índice na coleção ou o valor pontilhado da OID.</span><span class="sxs-lookup"><span data-stu-id="549c7-111">This can be either an index into the collection or the dotted value of the OID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="549c7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="549c7-112">Return value</span></span>

<span data-ttu-id="549c7-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="549c7-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="549c7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="549c7-114">Requirements</span></span>



| <span data-ttu-id="549c7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="549c7-115">Requirement</span></span> | <span data-ttu-id="549c7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="549c7-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="549c7-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="549c7-117">Redistributable</span></span><br/> | <span data-ttu-id="549c7-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="549c7-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="549c7-119">DLL</span><span class="sxs-lookup"><span data-stu-id="549c7-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="549c7-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="549c7-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
