---
description: Libera um bloqueio adquirido usando ExclusiveLock para o modo compartilhado.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'Método CShareLockNH:: ExclusiveUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755635"
---
# <a name="csharelocknhexclusiveunlock-method"></a><span data-ttu-id="ed97d-103">Método CShareLockNH:: ExclusiveUnlock</span><span class="sxs-lookup"><span data-stu-id="ed97d-103">CShareLockNH::ExclusiveUnlock method</span></span>

<span data-ttu-id="ed97d-104">Libera um bloqueio adquirido usando [**ExclusiveLock**](csharelocknh--exclusivelock.md) para o modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="ed97d-104">Releases a lock acquired by using [**ExclusiveLock**](csharelocknh--exclusivelock.md) to shared mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed97d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed97d-105">Syntax</span></span>


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a><span data-ttu-id="ed97d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed97d-106">Parameters</span></span>

<span data-ttu-id="ed97d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ed97d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed97d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed97d-108">Return value</span></span>

<span data-ttu-id="ed97d-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ed97d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed97d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed97d-110">Remarks</span></span>

<span data-ttu-id="ed97d-111">Cada chamada para [**ExclusiveLock**](csharelocknh--exclusivelock.md) deve ser emparelhada com exatamente uma chamada para **ExclusiveUnlock** para evitar o risco de um deadlock.</span><span class="sxs-lookup"><span data-stu-id="ed97d-111">Each call to [**ExclusiveLock**](csharelocknh--exclusivelock.md) must be paired with exactly one call to **ExclusiveUnlock** to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="ed97d-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ed97d-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed97d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed97d-113">Requirements</span></span>



| <span data-ttu-id="ed97d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed97d-114">Requirement</span></span> | <span data-ttu-id="ed97d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ed97d-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed97d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ed97d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ed97d-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed97d-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed97d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed97d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed97d-119">**ExclusiveLock**</span><span class="sxs-lookup"><span data-stu-id="ed97d-119">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
