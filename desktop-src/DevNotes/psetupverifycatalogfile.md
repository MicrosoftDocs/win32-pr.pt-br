---
description: Verifica um único arquivo de catálogo usando a política de assinatura de código do sistema operacional padrão, como assinatura de driver.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: função pSetupVerifyCatalogFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747871"
---
# <a name="psetupverifycatalogfile-function"></a><span data-ttu-id="c5c9a-103">função pSetupVerifyCatalogFile</span><span class="sxs-lookup"><span data-stu-id="c5c9a-103">pSetupVerifyCatalogFile function</span></span>

<span data-ttu-id="c5c9a-104">\[Esta função não é mais suportada pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5c9a-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="c5c9a-105">Para um arquivo INF (instalação do dispositivo), os desenvolvedores devem usar o **SetupVerifyInfFile**.</span><span class="sxs-lookup"><span data-stu-id="c5c9a-105">For an INF file (device install), developers should use **SetupVerifyInfFile**.</span></span> <span data-ttu-id="c5c9a-106">Para validar um catálogo não baseado em INF, use **WinVerifyTrust**.\]</span><span class="sxs-lookup"><span data-stu-id="c5c9a-106">To validate a non-INF based catalog, use **WinVerifyTrust**.\]</span></span>

<span data-ttu-id="c5c9a-107">Verifica um único arquivo de catálogo usando a política de assinatura de código do sistema operacional padrão, como assinatura de driver.</span><span class="sxs-lookup"><span data-stu-id="c5c9a-107">Verifies a single catalog file using standard operating system code signing policy, such as driver signing.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5c9a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5c9a-108">Syntax</span></span>


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="c5c9a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5c9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5c9a-110">*CatalogFullPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5c9a-110">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5c9a-111">O caminho totalmente qualificado do arquivo de catálogo a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="c5c9a-111">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5c9a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5c9a-112">Return value</span></span>

<span data-ttu-id="c5c9a-113">Se a função for bem-sucedida, ela retornará **\_ êxito de erro**; caso contrário, retornará o erro de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span><span class="sxs-lookup"><span data-stu-id="c5c9a-113">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

## <a name="remarks"></a><span data-ttu-id="c5c9a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5c9a-114">Remarks</span></span>

<span data-ttu-id="c5c9a-115">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="c5c9a-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5c9a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5c9a-116">Requirements</span></span>



| <span data-ttu-id="c5c9a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5c9a-117">Requirement</span></span> | <span data-ttu-id="c5c9a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c5c9a-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5c9a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c5c9a-119">DLL</span></span><br/> | <dl> <span data-ttu-id="c5c9a-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5c9a-120"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5c9a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5c9a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5c9a-122">**SetupVerifyInfFile**</span><span class="sxs-lookup"><span data-stu-id="c5c9a-122">**SetupVerifyInfFile**</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[<span data-ttu-id="c5c9a-123">**WinVerifyTrust**</span><span class="sxs-lookup"><span data-stu-id="c5c9a-123">**WinVerifyTrust**</span></span>](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
