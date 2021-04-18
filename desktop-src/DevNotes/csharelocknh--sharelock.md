---
description: Obtém um bloqueio compartilhado.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'Método CShareLockNH:: ShareLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751556"
---
# <a name="csharelocknhsharelock-method"></a><span data-ttu-id="c0e1c-103">Método CShareLockNH:: ShareLock</span><span class="sxs-lookup"><span data-stu-id="c0e1c-103">CShareLockNH::ShareLock method</span></span>

<span data-ttu-id="c0e1c-104">Obtém um bloqueio compartilhado.</span><span class="sxs-lookup"><span data-stu-id="c0e1c-104">Obtains a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0e1c-105">Syntax</span></span>


```C++
void ShareLock();
```



## <a name="parameters"></a><span data-ttu-id="c0e1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0e1c-106">Parameters</span></span>

<span data-ttu-id="c0e1c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c0e1c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0e1c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0e1c-108">Return value</span></span>

<span data-ttu-id="c0e1c-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c0e1c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e1c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0e1c-110">Remarks</span></span>

<span data-ttu-id="c0e1c-111">Cada chamada para **ShareLock** deve ser emparelhada com exatamente uma chamada para [**ShareUnlock**](csharelocknh--shareunlock.md).</span><span class="sxs-lookup"><span data-stu-id="c0e1c-111">Each call to **ShareLock** must be paired with exactly one call to [**ShareUnlock**](csharelocknh--shareunlock.md).</span></span> <span data-ttu-id="c0e1c-112">Somente um thread que chama **ShareLock** com êxito pode chamar **ShareUnlock**; caso contrário, pode ocorrer um deadlock.</span><span class="sxs-lookup"><span data-stu-id="c0e1c-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="c0e1c-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c0e1c-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0e1c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0e1c-114">Requirements</span></span>



| <span data-ttu-id="c0e1c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0e1c-115">Requirement</span></span> | <span data-ttu-id="c0e1c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c0e1c-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e1c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c0e1c-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c0e1c-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0e1c-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0e1c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0e1c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e1c-120">**ShareUnlock**</span><span class="sxs-lookup"><span data-stu-id="c0e1c-120">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
