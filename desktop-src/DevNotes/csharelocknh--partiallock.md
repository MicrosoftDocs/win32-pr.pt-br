---
description: Impede que mais de um thread conclua a aquisição de um bloqueio.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: 'CShareLockNH: método artialLock de:P'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751291"
---
# <a name="csharelocknhpartiallock-method"></a><span data-ttu-id="66f28-103">CShareLockNH: método artialLock de:P</span><span class="sxs-lookup"><span data-stu-id="66f28-103">CShareLockNH::PartialLock method</span></span>

<span data-ttu-id="66f28-104">Impede que mais de um thread conclua a aquisição de um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="66f28-104">Prevents more than one thread from completing acquiring a lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f28-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66f28-105">Syntax</span></span>


```C++
void PartialLock();
```



## <a name="parameters"></a><span data-ttu-id="66f28-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f28-106">Parameters</span></span>

<span data-ttu-id="66f28-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="66f28-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66f28-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66f28-108">Return value</span></span>

<span data-ttu-id="66f28-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="66f28-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66f28-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="66f28-110">Remarks</span></span>

<span data-ttu-id="66f28-111">Embora **PartialLock** esteja em vigor, outros threads que chamam [**ShareLock**](csharelocknh--sharelock.md) podem entrar no bloqueio.</span><span class="sxs-lookup"><span data-stu-id="66f28-111">While **PartialLock** is in effect, other threads calling [**ShareLock**](csharelocknh--sharelock.md) can enter the lock.</span></span>

<span data-ttu-id="66f28-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="66f28-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f28-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f28-113">Requirements</span></span>



| <span data-ttu-id="66f28-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f28-114">Requirement</span></span> | <span data-ttu-id="66f28-115">Valor</span><span class="sxs-lookup"><span data-stu-id="66f28-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66f28-116">DLL</span><span class="sxs-lookup"><span data-stu-id="66f28-116">DLL</span></span><br/> | <dl> <span data-ttu-id="66f28-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66f28-117"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
