---
description: Adquire um bloqueio de leitor/gravador.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'Método CShareLockNH:: ExclusiveLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749867"
---
# <a name="csharelocknhexclusivelock-method"></a><span data-ttu-id="d2cac-103">Método CShareLockNH:: ExclusiveLock</span><span class="sxs-lookup"><span data-stu-id="d2cac-103">CShareLockNH::ExclusiveLock method</span></span>

<span data-ttu-id="d2cac-104">Adquire um bloqueio de leitor/gravador.</span><span class="sxs-lookup"><span data-stu-id="d2cac-104">Acquires a reader/writer lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2cac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2cac-105">Syntax</span></span>


```C++
void ExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="d2cac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2cac-106">Parameters</span></span>

<span data-ttu-id="d2cac-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d2cac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2cac-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2cac-108">Return value</span></span>

<span data-ttu-id="d2cac-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d2cac-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2cac-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2cac-110">Remarks</span></span>

<span data-ttu-id="d2cac-111">Cada chamada para **ExclusiveLock** deve ser emparelhada com exatamente uma chamada para [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) para evitar o risco de um deadlock.</span><span class="sxs-lookup"><span data-stu-id="d2cac-111">Each call to **ExclusiveLock** must be paired with exactly one call to [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="d2cac-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d2cac-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2cac-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2cac-113">Requirements</span></span>



| <span data-ttu-id="d2cac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2cac-114">Requirement</span></span> | <span data-ttu-id="d2cac-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d2cac-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d2cac-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d2cac-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d2cac-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2cac-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2cac-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2cac-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2cac-119">**ExclusiveUnlock**</span><span class="sxs-lookup"><span data-stu-id="d2cac-119">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
