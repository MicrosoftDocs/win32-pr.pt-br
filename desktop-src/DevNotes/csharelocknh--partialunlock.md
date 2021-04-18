---
description: Libera um bloqueio parcial para que outros aquisições de bloqueio exclusivos ou parciais agora possam entrar.
ms.assetid: 95a3e0d1-4e8b-4e30-b4fd-709b9db465de
title: 'CShareLockNH: método artialUnlock de:P'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 930c0f51e199c1668a70f2dd017b0280939b0710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752172"
---
# <a name="csharelocknhpartialunlock-method"></a><span data-ttu-id="56937-103">CShareLockNH: método artialUnlock de:P</span><span class="sxs-lookup"><span data-stu-id="56937-103">CShareLockNH::PartialUnlock method</span></span>

<span data-ttu-id="56937-104">Libera um bloqueio parcial para que outros aquisições de bloqueio exclusivos ou parciais agora possam entrar.</span><span class="sxs-lookup"><span data-stu-id="56937-104">Releases a partial lock so that other exclusive or partial lock acquirers can now enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="56937-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56937-105">Syntax</span></span>


```C++
void PartialUnlock();
```



## <a name="parameters"></a><span data-ttu-id="56937-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56937-106">Parameters</span></span>

<span data-ttu-id="56937-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="56937-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56937-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56937-108">Return value</span></span>

<span data-ttu-id="56937-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="56937-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="56937-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="56937-110">Remarks</span></span>

<span data-ttu-id="56937-111">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="56937-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="56937-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56937-112">Requirements</span></span>



| <span data-ttu-id="56937-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="56937-113">Requirement</span></span> | <span data-ttu-id="56937-114">Valor</span><span class="sxs-lookup"><span data-stu-id="56937-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="56937-115">DLL</span><span class="sxs-lookup"><span data-stu-id="56937-115">DLL</span></span><br/> | <dl> <span data-ttu-id="56937-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56937-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
