---
description: Instala um arquivo de catálogo.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: função pSetupInstallCatalog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748495"
---
# <a name="psetupinstallcatalog-function"></a><span data-ttu-id="64f62-103">função pSetupInstallCatalog</span><span class="sxs-lookup"><span data-stu-id="64f62-103">pSetupInstallCatalog function</span></span>

<span data-ttu-id="64f62-104">\[Esta função não é mais suportada pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64f62-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="64f62-105">Os desenvolvedores devem usar o **CryptCATAdminAddCatalog**.\]</span><span class="sxs-lookup"><span data-stu-id="64f62-105">Developers should use **CryptCATAdminAddCatalog**.\]</span></span>

<span data-ttu-id="64f62-106">Instala um arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="64f62-106">Installs a catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f62-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64f62-107">Syntax</span></span>


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="64f62-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64f62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f62-109">*CatalogFullPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="64f62-109">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f62-110">O caminho totalmente qualificado do catálogo a ser instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="64f62-110">The fully qualified path of the catalog to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="64f62-111">*NewBaseName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="64f62-111">*NewBaseName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f62-112">O novo nome de base a ser usado quando o arquivo de catálogo é copiado para o repositório de catálogo.</span><span class="sxs-lookup"><span data-stu-id="64f62-112">The new base name to use when the catalog file is copied into the catalog store.</span></span>

</dd> <dt>

<span data-ttu-id="64f62-113">*NewCatalogFullPath* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="64f62-113">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="64f62-114">Opcionalmente, recebe o caminho totalmente qualificado do arquivo de catálogo no repositório de catálogo.</span><span class="sxs-lookup"><span data-stu-id="64f62-114">Optionally receives the fully qualified path of the catalog file within the catalog store.</span></span> <span data-ttu-id="64f62-115">Esse buffer deve ter no mínimo bytes de **\_ caminho máximo** (versão ANSI) ou caracteres (versão Unicode).</span><span class="sxs-lookup"><span data-stu-id="64f62-115">This buffer should be at least **MAX\_PATH** bytes (ANSI version) or chars (Unicode version).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f62-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64f62-116">Return value</span></span>

<span data-ttu-id="64f62-117">Se a função tiver êxito, ela **não retornará nenhum \_ erro**; caso contrário, ela retornará um código de erro Win32 que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="64f62-117">If the function succeeds, it returns **NO\_ERROR**; otherwise, it returns a Win32 error code that indicates the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f62-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="64f62-118">Remarks</span></span>

<span data-ttu-id="64f62-119">O arquivo é copiado pelo sistema em um diretório especial e, opcionalmente, é renomeado.</span><span class="sxs-lookup"><span data-stu-id="64f62-119">The file is copied by the system into a special directory and is optionally renamed.</span></span>

<span data-ttu-id="64f62-120">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="64f62-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f62-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64f62-121">Requirements</span></span>



| <span data-ttu-id="64f62-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="64f62-122">Requirement</span></span> | <span data-ttu-id="64f62-123">Valor</span><span class="sxs-lookup"><span data-stu-id="64f62-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64f62-124">DLL</span><span class="sxs-lookup"><span data-stu-id="64f62-124">DLL</span></span><br/> | <dl> <span data-ttu-id="64f62-125"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64f62-125"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64f62-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="64f62-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f62-127">**CryptCATAdminAddCatalog**</span><span class="sxs-lookup"><span data-stu-id="64f62-127">**CryptCATAdminAddCatalog**</span></span>](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
