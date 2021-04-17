---
description: A função GetDllVersion recupera o número de versão de Cabinet.dll.
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: Função GetDllVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 1b1142bd2ece965a3f2fc58b6bb2f90586a8b391
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754787"
---
# <a name="getdllversion-function"></a><span data-ttu-id="843cf-103">Função GetDllVersion</span><span class="sxs-lookup"><span data-stu-id="843cf-103">GetDllVersion function</span></span>

<span data-ttu-id="843cf-104">\[Essa função não é mais suportada, portanto, seu comportamento não pode ser garantido.</span><span class="sxs-lookup"><span data-stu-id="843cf-104">\[This function is no longer supported, so its behavior cannot be guaranteed.</span></span> <span data-ttu-id="843cf-105">\]</span><span class="sxs-lookup"><span data-stu-id="843cf-105">\]</span></span>

<span data-ttu-id="843cf-106">A função **GetDllVersion** recupera o número de versão de Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="843cf-106">The **GetDllVersion** function retrieves the version number of Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="843cf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="843cf-107">Syntax</span></span>


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a><span data-ttu-id="843cf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="843cf-108">Parameters</span></span>

<span data-ttu-id="843cf-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="843cf-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="843cf-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="843cf-110">Return value</span></span>

<span data-ttu-id="843cf-111">O número de versão do arquivo (consulte o [recurso VERSIONINFO](../menurc/versioninfo-resource.md)).</span><span class="sxs-lookup"><span data-stu-id="843cf-111">The version number of the file (see [VERSIONINFO Resource](../menurc/versioninfo-resource.md)).</span></span>

## <a name="remarks"></a><span data-ttu-id="843cf-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="843cf-112">Remarks</span></span>

<span data-ttu-id="843cf-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="843cf-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="843cf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="843cf-114">Requirements</span></span>



| <span data-ttu-id="843cf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="843cf-115">Requirement</span></span> | <span data-ttu-id="843cf-116">Valor</span><span class="sxs-lookup"><span data-stu-id="843cf-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="843cf-117">DLL</span><span class="sxs-lookup"><span data-stu-id="843cf-117">DLL</span></span><br/> | <dl> <span data-ttu-id="843cf-118"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="843cf-118"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="843cf-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="843cf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843cf-120">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="843cf-120">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 
