---
description: Indica a versão do CTL3D que está em execução no momento.
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Função Ctl3dGetVer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: e548d8933538ea85ba94f6e120032453079d69ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751754"
---
# <a name="ctl3dgetver-function"></a><span data-ttu-id="7cd6f-103">Função Ctl3dGetVer</span><span class="sxs-lookup"><span data-stu-id="7cd6f-103">Ctl3dGetVer function</span></span>

<span data-ttu-id="7cd6f-104">Indica a versão do CTL3D que está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="7cd6f-104">Indicates the version of CTL3D that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd6f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cd6f-105">Syntax</span></span>


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a><span data-ttu-id="7cd6f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cd6f-106">Parameters</span></span>

<span data-ttu-id="7cd6f-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7cd6f-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7cd6f-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7cd6f-108">Return value</span></span>

<span data-ttu-id="7cd6f-109">Retorna um valor que contém o número de versão principal no byte de ordem superior e o número de versão secundária no byte de ordem inferior.</span><span class="sxs-lookup"><span data-stu-id="7cd6f-109">Returns a value that contains the major version number in the high-order byte and the minor version number in the low-order byte.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd6f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cd6f-110">Remarks</span></span>

<span data-ttu-id="7cd6f-111">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7cd6f-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd6f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cd6f-112">Requirements</span></span>



| <span data-ttu-id="7cd6f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cd6f-113">Requirement</span></span> | <span data-ttu-id="7cd6f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7cd6f-114">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd6f-115">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd6f-115">DLL</span></span><br/> | <dl> <span data-ttu-id="7cd6f-116"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd6f-116"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
