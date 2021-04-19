---
description: Determina se Arquivos Offline está habilitado.
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: Função CSCIsCSCEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 13db7ebbb11f678c00a5a755ffe8114f8684b315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748846"
---
# <a name="csciscscenabled-function"></a><span data-ttu-id="bbafc-103">Função CSCIsCSCEnabled</span><span class="sxs-lookup"><span data-stu-id="bbafc-103">CSCIsCSCEnabled function</span></span>

<span data-ttu-id="bbafc-104">\[Essa função não tem suporte e não deve ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="bbafc-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="bbafc-105">Determina se Arquivos Offline está habilitado.</span><span class="sxs-lookup"><span data-stu-id="bbafc-105">Determines whether Offline Files is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbafc-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bbafc-106">Syntax</span></span>


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a><span data-ttu-id="bbafc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bbafc-107">Parameters</span></span>

<span data-ttu-id="bbafc-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bbafc-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbafc-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bbafc-109">Return value</span></span>

<span data-ttu-id="bbafc-110">Essa função retornará **true** se arquivos offline estiver habilitado e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="bbafc-110">This function returns **TRUE** if Offline Files is enabled and **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbafc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbafc-111">Remarks</span></span>

<span data-ttu-id="bbafc-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="bbafc-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbafc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbafc-113">Requirements</span></span>



| <span data-ttu-id="bbafc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbafc-114">Requirement</span></span> | <span data-ttu-id="bbafc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bbafc-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbafc-116">DLL</span><span class="sxs-lookup"><span data-stu-id="bbafc-116">DLL</span></span><br/> | <dl> <span data-ttu-id="bbafc-117"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbafc-117"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbafc-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbafc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbafc-119">**CSCQueryDatabaseStatus**</span><span class="sxs-lookup"><span data-stu-id="bbafc-119">**CSCQueryDatabaseStatus**</span></span>](cscquerydatabasestatus.md)
</dt> </dl>

 

 
