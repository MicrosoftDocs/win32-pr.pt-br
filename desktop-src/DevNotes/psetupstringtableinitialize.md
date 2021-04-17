---
description: Inicializa uma tabela de cadeia de caracteres.
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: função pSetupStringTableInitialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 67436dd0befbef01c5b6f55a68082b9e23870592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755275"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="4ed6e-103">função pSetupStringTableInitialize</span><span class="sxs-lookup"><span data-stu-id="4ed6e-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="4ed6e-104">\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="4ed6e-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="4ed6e-105">Inicializa uma tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ed6e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ed6e-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="4ed6e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ed6e-107">Parameters</span></span>

<span data-ttu-id="4ed6e-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4ed6e-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed6e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ed6e-109">Remarks</span></span>

<span data-ttu-id="4ed6e-110">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4ed6e-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed6e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ed6e-111">Requirements</span></span>



| <span data-ttu-id="4ed6e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ed6e-112">Requirement</span></span> | <span data-ttu-id="4ed6e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4ed6e-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed6e-114">DLL</span><span class="sxs-lookup"><span data-stu-id="4ed6e-114">DLL</span></span><br/> | <dl> <span data-ttu-id="4ed6e-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ed6e-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
