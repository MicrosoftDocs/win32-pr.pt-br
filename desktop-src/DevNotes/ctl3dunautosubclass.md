---
description: Desativa a subclasse automática.
ms.assetid: 85e5689f-6805-4aad-b97c-aa496e315900
title: Função Ctl3dUnAutoSubclass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 1250deb16307400898c92d36b9dda214115ec01d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751958"
---
# <a name="ctl3dunautosubclass-function"></a><span data-ttu-id="8fab3-103">Função Ctl3dUnAutoSubclass</span><span class="sxs-lookup"><span data-stu-id="8fab3-103">Ctl3dUnAutoSubclass function</span></span>

<span data-ttu-id="8fab3-104">Desativa a subclasse automática.</span><span class="sxs-lookup"><span data-stu-id="8fab3-104">Turns off automatic subclassing.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fab3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fab3-105">Syntax</span></span>


```C++
BOOL Ctl3dUnAutoSubclass(void);
```



## <a name="parameters"></a><span data-ttu-id="8fab3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fab3-106">Parameters</span></span>

<span data-ttu-id="8fab3-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8fab3-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fab3-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8fab3-108">Return value</span></span>

<span data-ttu-id="8fab3-109">Retornará **true** se a função tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="8fab3-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fab3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fab3-110">Remarks</span></span>

<span data-ttu-id="8fab3-111">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8fab3-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fab3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fab3-112">Requirements</span></span>



| <span data-ttu-id="8fab3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fab3-113">Requirement</span></span> | <span data-ttu-id="8fab3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="8fab3-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fab3-115">DLL</span><span class="sxs-lookup"><span data-stu-id="8fab3-115">DLL</span></span><br/> | <dl> <span data-ttu-id="8fab3-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fab3-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
