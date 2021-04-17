---
description: Libera um bloqueio compartilhado.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'Método CShareLockNH:: ShareUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755407"
---
# <a name="csharelocknhshareunlock-method"></a><span data-ttu-id="08abb-103">Método CShareLockNH:: ShareUnlock</span><span class="sxs-lookup"><span data-stu-id="08abb-103">CShareLockNH::ShareUnlock method</span></span>

<span data-ttu-id="08abb-104">Libera um bloqueio compartilhado.</span><span class="sxs-lookup"><span data-stu-id="08abb-104">Releases a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="08abb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08abb-105">Syntax</span></span>


```C++
void ShareUnlock();
```



## <a name="parameters"></a><span data-ttu-id="08abb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08abb-106">Parameters</span></span>

<span data-ttu-id="08abb-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="08abb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08abb-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08abb-108">Return value</span></span>

<span data-ttu-id="08abb-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="08abb-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08abb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="08abb-110">Remarks</span></span>

<span data-ttu-id="08abb-111">Cada chamada para [**ShareLock**](csharelocknh--sharelock.md) deve ser emparelhada com exatamente uma chamada para **ShareUnlock**.</span><span class="sxs-lookup"><span data-stu-id="08abb-111">Each call to [**ShareLock**](csharelocknh--sharelock.md) must be paired with exactly one call to **ShareUnlock**.</span></span> <span data-ttu-id="08abb-112">Somente um thread que chama **ShareLock** com êxito pode chamar **ShareUnlock**; caso contrário, pode ocorrer um deadlock.</span><span class="sxs-lookup"><span data-stu-id="08abb-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="08abb-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="08abb-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="08abb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08abb-114">Requirements</span></span>



| <span data-ttu-id="08abb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="08abb-115">Requirement</span></span> | <span data-ttu-id="08abb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="08abb-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="08abb-117">DLL</span><span class="sxs-lookup"><span data-stu-id="08abb-117">DLL</span></span><br/> | <dl> <span data-ttu-id="08abb-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08abb-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08abb-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="08abb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08abb-120">**ShareLock**</span><span class="sxs-lookup"><span data-stu-id="08abb-120">**ShareLock**</span></span>](csharelocknh--sharelock.md)
</dt> </dl>

 

 
