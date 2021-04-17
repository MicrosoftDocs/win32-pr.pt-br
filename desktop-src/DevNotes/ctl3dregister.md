---
description: Registra um aplicativo como um cliente do CTL3D.
ms.assetid: 38a4a04a-6322-4eb8-b272-ae9b90f84e0f
title: Função Ctl3dRegister
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dRegister
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 4b855c162d9d5f1c43a15d1ebd7219da6f847f37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748928"
---
# <a name="ctl3dregister-function"></a><span data-ttu-id="9b278-103">Função Ctl3dRegister</span><span class="sxs-lookup"><span data-stu-id="9b278-103">Ctl3dRegister function</span></span>

<span data-ttu-id="9b278-104">Registra um aplicativo como um cliente do CTL3D.</span><span class="sxs-lookup"><span data-stu-id="9b278-104">Registers an application as a client of CTL3D.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b278-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b278-105">Syntax</span></span>


```C++
BOOL Ctl3dRegister(
   HANDLE hinstApp
);
```



## <a name="parameters"></a><span data-ttu-id="9b278-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9b278-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b278-107">*hinstApp*</span><span class="sxs-lookup"><span data-stu-id="9b278-107">*hinstApp*</span></span> 
</dt> <dd>

<span data-ttu-id="9b278-108">Um identificador para o aplicativo a ser registrado como um cliente.</span><span class="sxs-lookup"><span data-stu-id="9b278-108">A handle to the application to be registered as a client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b278-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9b278-109">Return value</span></span>

<span data-ttu-id="9b278-110">Retornará **true** se os efeitos 3D estiverem ativos; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="9b278-110">Returns **TRUE** if 3D effects are active; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b278-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b278-111">Remarks</span></span>

<span data-ttu-id="9b278-112">Um aplicativo que usa CTL3D deve chamar essa função em WinMain.</span><span class="sxs-lookup"><span data-stu-id="9b278-112">An application that uses CTL3D should call this function in WinMain.</span></span>

<span data-ttu-id="9b278-113">os efeitos 3D não estão disponíveis em sistemas com resolução inferior a VGA.</span><span class="sxs-lookup"><span data-stu-id="9b278-113">3D effects are not available on systems that have less than VGA resolution.</span></span>

<span data-ttu-id="9b278-114">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9b278-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b278-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b278-115">Requirements</span></span>



| <span data-ttu-id="9b278-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b278-116">Requirement</span></span> | <span data-ttu-id="9b278-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9b278-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b278-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9b278-118">DLL</span></span><br/> | <dl> <span data-ttu-id="9b278-119"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b278-119"><dt>Ctl3d32.dll</dt></span></span> </dl> |



 

 
