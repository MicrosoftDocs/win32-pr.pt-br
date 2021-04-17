---
description: Cancela o registro de um aplicativo como um cliente do CTL3D.
ms.assetid: 21990A79-F90D-4AE1-AB02-2B33583B47F5
title: Função Ctl3dUnregister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dUnregister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85cd45062da9c01ef8af5a312a855bfaab6a6bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748517"
---
# <a name="ctl3dunregister-function"></a><span data-ttu-id="1e93e-103">Função Ctl3dUnregister</span><span class="sxs-lookup"><span data-stu-id="1e93e-103">Ctl3dUnregister function</span></span>

<span data-ttu-id="1e93e-104">Cancela o registro de um aplicativo como um cliente do CTL3D.</span><span class="sxs-lookup"><span data-stu-id="1e93e-104">Unregisters an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e93e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e93e-105">Syntax</span></span>


```C++
BOOL Ctl3dUnregister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="1e93e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e93e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e93e-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="1e93e-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="1e93e-108">Um identificador para o aplicativo ter o registro cancelado como um cliente.</span><span class="sxs-lookup"><span data-stu-id="1e93e-108">A handle to the application to be unregistered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e93e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e93e-109">Return value</span></span>

<span data-ttu-id="1e93e-110">Retornará **true** se o aplicativo tiver o registro cancelado como um cliente de CTL3D; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="1e93e-110">Returns **TRUE** if the application is unregistered as a client of CTL3D; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e93e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e93e-111">Remarks</span></span>

<span data-ttu-id="1e93e-112">Um aplicativo que usa CTL3D deve chamar essa função em WinMain.</span><span class="sxs-lookup"><span data-stu-id="1e93e-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="1e93e-113">os efeitos 3D não estão disponíveis em sistemas com resolução inferior a VGA.</span><span class="sxs-lookup"><span data-stu-id="1e93e-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="1e93e-114">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1e93e-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e93e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e93e-115">Requirements</span></span>



| <span data-ttu-id="1e93e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e93e-116">Requirement</span></span> | <span data-ttu-id="1e93e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1e93e-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e93e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="1e93e-118">DLL</span></span><br/> | <dl> <span data-ttu-id="1e93e-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e93e-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
