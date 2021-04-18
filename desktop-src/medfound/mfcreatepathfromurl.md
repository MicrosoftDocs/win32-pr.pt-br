---
description: Converte uma URL de arquivo em um caminho do Microsoft MS-DOS.
ms.assetid: c35988ad-6cf8-41ec-bee9-e3bb982310ee
title: Função MFCreatePathFromURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreatePathFromURL
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: c1838a3b09dc5375588d562aa503d555a186e394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780398"
---
# <a name="mfcreatepathfromurl-function"></a><span data-ttu-id="d199a-103">Função MFCreatePathFromURL</span><span class="sxs-lookup"><span data-stu-id="d199a-103">MFCreatePathFromURL function</span></span>

<span data-ttu-id="d199a-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="d199a-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d199a-105">Em vez disso, os aplicativos devem chamar [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span><span class="sxs-lookup"><span data-stu-id="d199a-105">Instead, applications should call [**PathCreateFromUrl**](/windows/win32/api/shlwapi/nf-shlwapi-pathcreatefromurla).\]</span></span>

<span data-ttu-id="d199a-106">Converte uma URL de arquivo em um caminho do Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="d199a-106">Converts a file URL to a Microsoft MS-DOS path.</span></span>

## <a name="syntax"></a><span data-ttu-id="d199a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d199a-107">Syntax</span></span>


```C++
HRESULT MFCreatePathFromURL(
  _In_opt_ LPCWSTR pwszFileURL,
  _Out_    LPWSTR  *ppwszFilePath
);
```



## <a name="parameters"></a><span data-ttu-id="d199a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d199a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d199a-109">*pwszFileURL* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d199a-109">*pwszFileURL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d199a-110">Uma cadeia de caracteres terminada em nulo que contém a URL.</span><span class="sxs-lookup"><span data-stu-id="d199a-110">A null-terminated string that contains the URL.</span></span> <span data-ttu-id="d199a-111">O comprimento máximo da cadeia de caracteres é o **\_ \_ \_ comprimento máximo da URL da Internet**.</span><span class="sxs-lookup"><span data-stu-id="d199a-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="d199a-112">*ppwszFilePath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d199a-112">*ppwszFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d199a-113">Recebe uma cadeia de caracteres terminada em nulo que contém a URL.</span><span class="sxs-lookup"><span data-stu-id="d199a-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="d199a-114">O chamador deve liberar a cadeia de caracteres chamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="d199a-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d199a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d199a-115">Return value</span></span>

<span data-ttu-id="d199a-116">A função retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d199a-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="d199a-117">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d199a-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d199a-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d199a-118">Return code</span></span>                                                                                  | <span data-ttu-id="d199a-119">Description</span><span class="sxs-lookup"><span data-stu-id="d199a-119">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d199a-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d199a-121">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d199a-121">The function succeeded.</span></span> <br/>                                                                         |
| <dl> <span data-ttu-id="d199a-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d199a-123">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="d199a-123">Invalid argument.</span></span> <span data-ttu-id="d199a-124">A cadeia de caracteres fornecida no parâmetro *pwszFileURL* não pode ser convertida em um caminho.</span><span class="sxs-lookup"><span data-stu-id="d199a-124">The string given in the *pwszFileURL* parameter cannot be converted to a path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d199a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d199a-125">Remarks</span></span>

<span data-ttu-id="d199a-126">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="d199a-126">This function has no associated import library.</span></span> <span data-ttu-id="d199a-127">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="d199a-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d199a-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d199a-128">Requirements</span></span>



| <span data-ttu-id="d199a-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d199a-129">Requirement</span></span> | <span data-ttu-id="d199a-130">Valor</span><span class="sxs-lookup"><span data-stu-id="d199a-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d199a-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d199a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d199a-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d199a-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d199a-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d199a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d199a-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d199a-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d199a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d199a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d199a-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d199a-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d199a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d199a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d199a-138">Funções de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d199a-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
