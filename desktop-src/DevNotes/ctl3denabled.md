---
description: Verifica se os controles podem usar efeitos 3D.
ms.assetid: fb7b892f-2580-41ac-b2ef-938da3cc1dc2
title: Função Ctl3dEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dEnabled
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: d0eecec5650ecc00b69c0745e58a3e1d0f931a00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750925"
---
# <a name="ctl3denabled-function"></a><span data-ttu-id="6cdcc-103">Função Ctl3dEnabled</span><span class="sxs-lookup"><span data-stu-id="6cdcc-103">Ctl3dEnabled function</span></span>

<span data-ttu-id="6cdcc-104">Verifica se os controles podem usar efeitos 3D.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-104">Verifies whether controls can use 3D effects.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cdcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cdcc-105">Syntax</span></span>


```C++
BOOL Ctl3dEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="6cdcc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cdcc-106">Parameters</span></span>

<span data-ttu-id="6cdcc-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6cdcc-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6cdcc-108">Return value</span></span>

<span data-ttu-id="6cdcc-109">Retornará **true** se os controles puderem usar efeitos 3D; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-109">Returns **TRUE** if controls can use 3D effects; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cdcc-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cdcc-110">Remarks</span></span>

<span data-ttu-id="6cdcc-111">No Windows 4,0 ou posterior, **Ctl3dEnabled** e [**Ctl3dRegister**](ctl3dregister.md) retornam **false**.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-111">In Windows 4.0 or later, **Ctl3dEnabled** and [**Ctl3dRegister**](ctl3dregister.md) return **FALSE**.</span></span>

<span data-ttu-id="6cdcc-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6cdcc-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cdcc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cdcc-113">Requirements</span></span>



| <span data-ttu-id="6cdcc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cdcc-114">Requirement</span></span> | <span data-ttu-id="6cdcc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6cdcc-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdcc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6cdcc-116">DLL</span></span><br/> | <dl> <span data-ttu-id="6cdcc-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cdcc-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
