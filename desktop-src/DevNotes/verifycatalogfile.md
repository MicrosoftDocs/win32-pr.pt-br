---
description: Verifica um único arquivo de catálogo.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: Função VerifyCatalogFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748925"
---
# <a name="verifycatalogfile-function"></a><span data-ttu-id="c7c5f-103">Função VerifyCatalogFile</span><span class="sxs-lookup"><span data-stu-id="c7c5f-103">VerifyCatalogFile function</span></span>

<span data-ttu-id="c7c5f-104">\[Essa função não tem suporte e não deve ser usada.\]</span><span class="sxs-lookup"><span data-stu-id="c7c5f-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="c7c5f-105">Verifica um único arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="c7c5f-105">Verifies a single catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c5f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7c5f-106">Syntax</span></span>


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="c7c5f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7c5f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c5f-108">*CatalogFullPath*</span><span class="sxs-lookup"><span data-stu-id="c7c5f-108">*CatalogFullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="c7c5f-109">O caminho totalmente qualificado do arquivo de catálogo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="c7c5f-109">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c5f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7c5f-110">Return value</span></span>

<span data-ttu-id="c7c5f-111">Se a função for bem-sucedida, ela retornará **\_ êxito de erro**; caso contrário, retornará o erro de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="c7c5f-111">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

<span data-ttu-id="c7c5f-112">Se o catálogo for um catálogo assinado por Authenticode, essa função retornará um **erro de \_ \_ \_ Publicador de Authenticode confiável** se tiver sucesso; caso contrário, ele retornará um **erro de confiança de \_ Authenticode \_ \_ não \_ estabelecida**.</span><span class="sxs-lookup"><span data-stu-id="c7c5f-112">If the catalog is an Authenticode-signed catalog, this function returns **ERROR\_AUTHENTICODE\_TRUSTED\_PUBLISHER** if it succeeds; otherwise, it returns **ERROR\_AUTHENTICODE\_TRUST\_NOT\_ESTABLISHED**.</span></span>

<span data-ttu-id="c7c5f-113">Se a função não puder determinar se o Publicador é confiável, ele também poderá retornar **um \_ \_ erro de erro não identificado**.</span><span class="sxs-lookup"><span data-stu-id="c7c5f-113">If the function is unable to determine whether the publisher is trusted, it may also return **ERROR\_UNIDENTIFIED\_ERROR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c5f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7c5f-114">Remarks</span></span>

<span data-ttu-id="c7c5f-115">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c7c5f-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7c5f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7c5f-116">Requirements</span></span>



| <span data-ttu-id="c7c5f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c5f-117">Requirement</span></span> | <span data-ttu-id="c7c5f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c7c5f-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c5f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c5f-119">DLL</span></span><br/> | <dl> <span data-ttu-id="c7c5f-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c5f-120"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
