---
description: Fecha um identificador de pesquisa.
ms.assetid: 2e6a547f-26a7-401a-b1e4-3f085ce82729
title: Função CSCFindClose
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindClose
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 69e3ea972ccd67a1db999c186709ef3aeff84be9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747627"
---
# <a name="cscfindclose-function"></a><span data-ttu-id="c1fa8-103">Função CSCFindClose</span><span class="sxs-lookup"><span data-stu-id="c1fa8-103">CSCFindClose function</span></span>

<span data-ttu-id="c1fa8-104">\[Essa função não tem suporte e não deve ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="c1fa8-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="c1fa8-105">Fecha um identificador de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c1fa8-105">Closes a search handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1fa8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1fa8-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindClose(
  _In_ HANDLE hFind
);
```



## <a name="parameters"></a><span data-ttu-id="c1fa8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1fa8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fa8-108">*hFind* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1fa8-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fa8-109">Um identificador de pesquisa retornado pela função [**CSCFindFirstFileW**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="c1fa8-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fa8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1fa8-110">Return value</span></span>

<span data-ttu-id="c1fa8-111">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="c1fa8-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1fa8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1fa8-112">Remarks</span></span>

<span data-ttu-id="c1fa8-113">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c1fa8-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1fa8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1fa8-114">Requirements</span></span>



| <span data-ttu-id="c1fa8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1fa8-115">Requirement</span></span> | <span data-ttu-id="c1fa8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c1fa8-116">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fa8-117">DLL</span><span class="sxs-lookup"><span data-stu-id="c1fa8-117">DLL</span></span><br/> | <dl> <span data-ttu-id="c1fa8-118"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1fa8-118"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1fa8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1fa8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1fa8-120">**CSCFindFirstFileW**</span><span class="sxs-lookup"><span data-stu-id="c1fa8-120">**CSCFindFirstFileW**</span></span>](cscfindfirstfilew.md)
</dt> </dl>

 

 
