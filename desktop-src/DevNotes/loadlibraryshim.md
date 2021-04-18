---
description: Carrega uma versão especificada de uma .NET Framework DLL da biblioteca.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: Função LoadLibraryShim
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771775"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="597dc-103">Função LoadLibraryShim</span><span class="sxs-lookup"><span data-stu-id="597dc-103">LoadLibraryShim function</span></span>

<span data-ttu-id="597dc-104">Carrega uma versão especificada de uma .NET Framework DLL da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="597dc-104">Loads a specified version of a .NET Framework library DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="597dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="597dc-105">Syntax</span></span>


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a><span data-ttu-id="597dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="597dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="597dc-107">*szDllName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="597dc-107">*szDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="597dc-108">O nome da DLL a ser carregada a partir da .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="597dc-108">The name of the DLL to be loaded from the .NET Framework.</span></span>

</dd> <dt>

<span data-ttu-id="597dc-109">*szVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="597dc-109">*szVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="597dc-110">A versão da DLL a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="597dc-110">The version of the DLL to be loaded.</span></span> <span data-ttu-id="597dc-111">Se *szVersion* for **NULL**, a versão mais recente da DLL especificada será carregada.</span><span class="sxs-lookup"><span data-stu-id="597dc-111">If *szVersion* is **NULL**, the latest version of the specified DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="597dc-112">*pvReserved*</span><span class="sxs-lookup"><span data-stu-id="597dc-112">*pvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="597dc-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="597dc-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="597dc-114">*phModDll* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="597dc-114">*phModDll* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="597dc-115">Um identificador para o módulo.</span><span class="sxs-lookup"><span data-stu-id="597dc-115">A handle to the module.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="597dc-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="597dc-116">Return value</span></span>

<span data-ttu-id="597dc-117">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="597dc-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="597dc-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="597dc-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="597dc-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="597dc-119">Remarks</span></span>

<span data-ttu-id="597dc-120">Essa função é usada para carregar DLLs de biblioteca incluídas no pacote redistribuível .NET Framework, não DLLs geradas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="597dc-120">This function is used to load library DLLs that are included in the .NET Framework redistributable package, not user-generated DLLs.</span></span>

<span data-ttu-id="597dc-121">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="597dc-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="597dc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="597dc-122">Requirements</span></span>



| <span data-ttu-id="597dc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="597dc-123">Requirement</span></span> | <span data-ttu-id="597dc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="597dc-124">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="597dc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="597dc-125">DLL</span></span><br/> | <dl> <span data-ttu-id="597dc-126"><dt>Mscoree.dll</dt></span><span class="sxs-lookup"><span data-stu-id="597dc-126"><dt>Mscoree.dll</dt></span></span> </dl> |



 

 
