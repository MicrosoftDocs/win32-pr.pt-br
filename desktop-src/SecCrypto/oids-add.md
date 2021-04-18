---
description: Adiciona o objeto OID especificado à coleção.
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Método OIDs. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811051"
---
# <a name="oidsadd-method"></a><span data-ttu-id="e4953-103">Método OIDs. Add</span><span class="sxs-lookup"><span data-stu-id="e4953-103">OIDs.Add method</span></span>

<span data-ttu-id="e4953-104">\[O método **Add** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e4953-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e4953-105">Em vez disso, use a [**classe OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e4953-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e4953-106">O método **Add** adiciona o objeto [**OID**](oid.md) especificado à coleção.</span><span class="sxs-lookup"><span data-stu-id="e4953-106">The **Add** method adds the specified [**OID**](oid.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4953-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4953-107">Syntax</span></span>


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a><span data-ttu-id="e4953-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4953-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4953-109">*OID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4953-109">*OID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4953-110">O objeto de [**OID**](oid.md) a ser adicionado à coleção.</span><span class="sxs-lookup"><span data-stu-id="e4953-110">The [**OID**](oid.md) object to be added to the collection.</span></span> <span data-ttu-id="e4953-111">O objeto **OID** é adicionado na ordem classificada com base em seu valor pontilhado.</span><span class="sxs-lookup"><span data-stu-id="e4953-111">The **OID** object is added in sorted order based on its dotted value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4953-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4953-112">Return value</span></span>

<span data-ttu-id="e4953-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e4953-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4953-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4953-114">Requirements</span></span>



| <span data-ttu-id="e4953-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4953-115">Requirement</span></span> | <span data-ttu-id="e4953-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e4953-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4953-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e4953-117">Redistributable</span></span><br/> | <span data-ttu-id="e4953-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4953-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e4953-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e4953-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="e4953-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4953-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
