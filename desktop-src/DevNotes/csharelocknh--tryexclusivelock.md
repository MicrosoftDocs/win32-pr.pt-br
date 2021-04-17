---
description: Obtém um bloqueio exclusivamente se nenhum outro estiver mantendo-o no momento.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: 'Método CShareLockNH:: TryExclusiveLock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8465e247807c4229821acef552e0786a5604a3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747884"
---
# <a name="csharelocknhtryexclusivelock-method"></a><span data-ttu-id="7e648-103">Método CShareLockNH:: TryExclusiveLock</span><span class="sxs-lookup"><span data-stu-id="7e648-103">CShareLockNH::TryExclusiveLock method</span></span>

<span data-ttu-id="7e648-104">Obtém um bloqueio exclusivamente se nenhum outro estiver mantendo-o no momento.</span><span class="sxs-lookup"><span data-stu-id="7e648-104">Obtains a lock exclusively if no others are currently hold it.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e648-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e648-105">Syntax</span></span>


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="7e648-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e648-106">Parameters</span></span>

<span data-ttu-id="7e648-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7e648-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e648-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e648-108">Return value</span></span>

<span data-ttu-id="7e648-109">Retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="7e648-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e648-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e648-110">Remarks</span></span>

<span data-ttu-id="7e648-111">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7e648-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e648-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e648-112">Requirements</span></span>



| <span data-ttu-id="7e648-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e648-113">Requirement</span></span> | <span data-ttu-id="7e648-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7e648-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7e648-115">DLL</span><span class="sxs-lookup"><span data-stu-id="7e648-115">DLL</span></span><br/> | <dl> <span data-ttu-id="7e648-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e648-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
