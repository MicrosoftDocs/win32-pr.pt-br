---
description: Recupera informações sobre o espaço usado pelo cache Arquivos Offline.
ms.assetid: 3a6fa548-0e9a-4138-a5ec-cde0aeb2b811
title: Função CSCGetSpaceUsageW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCGetSpaceUsageW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 608fd7736093ae1f8d131ede777a691e467de9de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748910"
---
# <a name="cscgetspaceusagew-function"></a><span data-ttu-id="823fd-103">Função CSCGetSpaceUsageW</span><span class="sxs-lookup"><span data-stu-id="823fd-103">CSCGetSpaceUsageW function</span></span>

<span data-ttu-id="823fd-104">\[Essa função não tem suporte e não deve ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="823fd-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="823fd-105">Recupera informações sobre o espaço usado pelo cache Arquivos Offline.</span><span class="sxs-lookup"><span data-stu-id="823fd-105">Retrieves information about the space used by the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="823fd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="823fd-106">Syntax</span></span>


```C++
BOOL WINAPI CSCGetSpaceUsageW(
  _Inout_ LPTSTR  lptzLocation,
  _In_    DWORD   dwSize,
  _Inout_ LPDWORD lpdwMaxSpaceHigh,
  _Inout_ LPDWORD lpdwMaxSpaceLow,
  _Inout_ LPDWORD lpdwCurrentSpaceHigh,
  _Inout_ LPDWORD lpdwCurrentSpaceLow,
  _Inout_ LPDWORD lpcntTotalFiles,
  _Inout_ LPDWORD lpcntTotalDirs
);
```



## <a name="parameters"></a><span data-ttu-id="823fd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="823fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="823fd-108">*lptzLocation* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="823fd-108">*lptzLocation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="823fd-109">O local do diretório do cache.</span><span class="sxs-lookup"><span data-stu-id="823fd-109">The directory location of the cache.</span></span>

</dd> <dt>

<span data-ttu-id="823fd-110">*dwSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="823fd-110">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="823fd-111">O tamanho do buffer *lptzLocation* , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="823fd-111">The size of the *lptzLocation* buffer, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="823fd-112">*lpdwMaxSpaceHigh* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="823fd-112">*lpdwMaxSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="823fd-113">A **DWORD** de ordem superior do número máximo de bytes disponíveis no cache.</span><span class="sxs-lookup"><span data-stu-id="823fd-113">The high-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="823fd-114">*lpdwMaxSpaceLow* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="823fd-114">*lpdwMaxSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="823fd-115">A **DWORD** de ordem inferior do número máximo de bytes disponíveis no cache.</span><span class="sxs-lookup"><span data-stu-id="823fd-115">The low-order **DWORD** of the maximum number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="823fd-116">*lpdwCurrentSpaceHigh* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="823fd-116">*lpdwCurrentSpaceHigh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="823fd-117">A **DWORD** de ordem superior do número atual de bytes disponíveis no cache.</span><span class="sxs-lookup"><span data-stu-id="823fd-117">The high-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="823fd-118">*lpdwCurrentSpaceLow* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="823fd-118">*lpdwCurrentSpaceLow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="823fd-119">A **DWORD** de ordem inferior do número atual de bytes disponíveis no cache.</span><span class="sxs-lookup"><span data-stu-id="823fd-119">The low-order **DWORD** of the current number of bytes available in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="823fd-120">*lpcntTotalFiles* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="823fd-120">*lpcntTotalFiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="823fd-121">O número total de arquivos no cache.</span><span class="sxs-lookup"><span data-stu-id="823fd-121">The total number of files in the cache.</span></span>

</dd> <dt>

<span data-ttu-id="823fd-122">*lpcntTotalDirs* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="823fd-122">*lpcntTotalDirs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="823fd-123">O número total de diretórios no cache.</span><span class="sxs-lookup"><span data-stu-id="823fd-123">The total number of directories in the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="823fd-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="823fd-124">Return value</span></span>

<span data-ttu-id="823fd-125">Essa função retornará **true** se tiver sucesso; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="823fd-125">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="823fd-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="823fd-126">Remarks</span></span>

<span data-ttu-id="823fd-127">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="823fd-127">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="823fd-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="823fd-128">Requirements</span></span>



| <span data-ttu-id="823fd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="823fd-129">Requirement</span></span> | <span data-ttu-id="823fd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="823fd-130">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="823fd-131">DLL</span><span class="sxs-lookup"><span data-stu-id="823fd-131">DLL</span></span><br/> | <dl> <span data-ttu-id="823fd-132"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="823fd-132"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
