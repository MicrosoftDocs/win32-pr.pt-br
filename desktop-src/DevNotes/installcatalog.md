---
description: Instala um catálogo em um diretório.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: Função InstallCatalog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756513"
---
# <a name="installcatalog-function"></a><span data-ttu-id="6d559-103">Função InstallCatalog</span><span class="sxs-lookup"><span data-stu-id="6d559-103">InstallCatalog function</span></span>

<span data-ttu-id="6d559-104">\[Essa função não tem suporte e não deve ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="6d559-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="6d559-105">Instala um catálogo em um diretório.</span><span class="sxs-lookup"><span data-stu-id="6d559-105">Installs a catalog in a directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d559-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d559-106">Syntax</span></span>


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="6d559-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d559-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d559-108">*CatalogFullPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d559-108">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d559-109">Um ponteiro para uma cadeia de caracteres que representa o caminho completo do catálogo antes da instalação.</span><span class="sxs-lookup"><span data-stu-id="6d559-109">A pointer to a string that represents the full path of the catalog before installation.</span></span>

</dd> <dt>

<span data-ttu-id="6d559-110">*NewBaseName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6d559-110">*NewBaseName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d559-111">Um ponteiro para o novo nome de base.</span><span class="sxs-lookup"><span data-stu-id="6d559-111">A pointer to the new base name.</span></span>

</dd> <dt>

<span data-ttu-id="6d559-112">*NewCatalogFullPath* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6d559-112">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d559-113">Um ponteiro para uma cadeia de caracteres que representa o caminho completo do catálogo após a instalação.</span><span class="sxs-lookup"><span data-stu-id="6d559-113">A pointer to a string that represent the full path of the catalog after installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d559-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d559-114">Return value</span></span>

<span data-ttu-id="6d559-115">Essa função não está implementada no momento, portanto, não retorna um valor real.</span><span class="sxs-lookup"><span data-stu-id="6d559-115">This function is not currently implemented, so it does not return an actual value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d559-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d559-116">Remarks</span></span>

<span data-ttu-id="6d559-117">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6d559-117">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d559-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d559-118">Requirements</span></span>



| <span data-ttu-id="6d559-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d559-119">Requirement</span></span> | <span data-ttu-id="6d559-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6d559-120">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d559-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6d559-121">DLL</span></span><br/> | <dl> <span data-ttu-id="6d559-122"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d559-122"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
