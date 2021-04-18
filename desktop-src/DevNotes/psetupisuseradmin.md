---
description: Indica se o usuário atual é um administrador.
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: função pSetupIsUserAdmin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1c40a69fd682c22e2625a3ba362d11d719cf9cce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756104"
---
# <a name="psetupisuseradmin-function"></a><span data-ttu-id="4b8cb-103">função pSetupIsUserAdmin</span><span class="sxs-lookup"><span data-stu-id="4b8cb-103">pSetupIsUserAdmin function</span></span>

<span data-ttu-id="4b8cb-104">\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="4b8cb-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="4b8cb-105">Indica se o usuário atual é um administrador.</span><span class="sxs-lookup"><span data-stu-id="4b8cb-105">Indicates whether the current user is an administrator.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8cb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b8cb-106">Syntax</span></span>


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a><span data-ttu-id="4b8cb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b8cb-107">Parameters</span></span>

<span data-ttu-id="4b8cb-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b8cb-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b8cb-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4b8cb-109">Return value</span></span>

<span data-ttu-id="4b8cb-110">**True** se o usuário atual for um administrador, caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="4b8cb-110">**TRUE** if the current user is an administrator, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b8cb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b8cb-111">Remarks</span></span>

<span data-ttu-id="4b8cb-112">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4b8cb-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8cb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b8cb-113">Requirements</span></span>



| <span data-ttu-id="4b8cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8cb-114">Requirement</span></span> | <span data-ttu-id="4b8cb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4b8cb-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8cb-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4b8cb-116">DLL</span></span><br/> | <dl> <span data-ttu-id="4b8cb-117"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b8cb-117"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
