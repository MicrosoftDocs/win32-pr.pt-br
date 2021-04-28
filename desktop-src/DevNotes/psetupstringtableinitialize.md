---
description: função pSetupStringTableInitialize – Inicializa uma tabela de cadeia de caracteres.
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
ms.openlocfilehash: 79638f9f1f80f4b9b3d54a33c7e94234174ffb19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089195"
---
# <a name="psetupstringtableinitialize-function"></a><span data-ttu-id="bdd8a-103">função pSetupStringTableInitialize</span><span class="sxs-lookup"><span data-stu-id="bdd8a-103">pSetupStringTableInitialize function</span></span>

<span data-ttu-id="bdd8a-104">\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="bdd8a-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="bdd8a-105">Inicializa uma tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd8a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bdd8a-106">Syntax</span></span>


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="bdd8a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdd8a-107">Parameters</span></span>

<span data-ttu-id="bdd8a-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bdd8a-108">This function has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdd8a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdd8a-109">Remarks</span></span>

<span data-ttu-id="bdd8a-110">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="bdd8a-110">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd8a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdd8a-111">Requirements</span></span>



| <span data-ttu-id="bdd8a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd8a-112">Requirement</span></span> | <span data-ttu-id="bdd8a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="bdd8a-113">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd8a-114">DLL</span><span class="sxs-lookup"><span data-stu-id="bdd8a-114">DLL</span></span><br/> | <dl> <span data-ttu-id="bdd8a-115"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdd8a-115"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
