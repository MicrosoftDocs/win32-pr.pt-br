---
description: Altera um bloqueio compartilhado para um bloqueio parcial.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'Método CShareLockNH:: SharedToPartial'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753772"
---
# <a name="csharelocknhsharedtopartial-method"></a><span data-ttu-id="fb1a6-103">Método CShareLockNH:: SharedToPartial</span><span class="sxs-lookup"><span data-stu-id="fb1a6-103">CShareLockNH::SharedToPartial method</span></span>

<span data-ttu-id="fb1a6-104">Altera um bloqueio compartilhado para um bloqueio parcial.</span><span class="sxs-lookup"><span data-stu-id="fb1a6-104">Changes a shared lock to a partial lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb1a6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb1a6-105">Syntax</span></span>


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a><span data-ttu-id="fb1a6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb1a6-106">Parameters</span></span>

<span data-ttu-id="fb1a6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fb1a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb1a6-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb1a6-108">Return value</span></span>

<span data-ttu-id="fb1a6-109">Retornará **true** se o bloqueio parcial for obtido; caso contrário, retornará **false** e o bloqueio permanecerá no modo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="fb1a6-109">Returns **TRUE** if the partial lock is obtained; otherwise, it returns **FALSE** and the lock remains in shared mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb1a6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb1a6-110">Remarks</span></span>

<span data-ttu-id="fb1a6-111">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fb1a6-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb1a6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb1a6-112">Requirements</span></span>



| <span data-ttu-id="fb1a6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb1a6-113">Requirement</span></span> | <span data-ttu-id="fb1a6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fb1a6-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fb1a6-115">DLL</span><span class="sxs-lookup"><span data-stu-id="fb1a6-115">DLL</span></span><br/> | <dl> <span data-ttu-id="fb1a6-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb1a6-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
