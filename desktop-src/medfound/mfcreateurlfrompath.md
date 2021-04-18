---
description: Converte um caminho do Microsoft MS-DOS em uma URL canônica.
ms.assetid: 1186b970-9ae1-4020-b999-55157cff1741
title: Função MFCreateURLFromPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateURLFromPath
api_type:
- DllExport
api_location:
- mfplat.dll
ms.openlocfilehash: e43c2d7df299792d8b5be99226e9cfdbd11976a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793684"
---
# <a name="mfcreateurlfrompath-function"></a><span data-ttu-id="6cce9-103">Função MFCreateURLFromPath</span><span class="sxs-lookup"><span data-stu-id="6cce9-103">MFCreateURLFromPath function</span></span>

<span data-ttu-id="6cce9-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="6cce9-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="6cce9-105">Em vez disso, os aplicativos devem chamar [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span><span class="sxs-lookup"><span data-stu-id="6cce9-105">Instead, Applications should call [UrlCreateFromPath](/windows/desktop/api/shlwapi/nf-shlwapi-urlcreatefrompatha).\]</span></span>

<span data-ttu-id="6cce9-106">Converte um caminho do Microsoft MS-DOS em uma URL canônica.</span><span class="sxs-lookup"><span data-stu-id="6cce9-106">Converts a Microsoft MS-DOS path to a canonicalized URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cce9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cce9-107">Syntax</span></span>


```C++
HRESULT MFCreateURLFromPath(
  _In_opt_ LPCWSTR pwszFilePath,
  _Out_    LPWSTR  *ppwszFileURL
);
```



## <a name="parameters"></a><span data-ttu-id="6cce9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cce9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cce9-109">*pwszFilePath* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6cce9-109">*pwszFilePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cce9-110">Uma cadeia de caracteres terminada em nulo que contém o caminho.</span><span class="sxs-lookup"><span data-stu-id="6cce9-110">A null-terminated string that contains the path.</span></span> <span data-ttu-id="6cce9-111">O comprimento máximo da cadeia de caracteres é o **\_ \_ \_ comprimento máximo da URL da Internet**.</span><span class="sxs-lookup"><span data-stu-id="6cce9-111">The maximum length of the string is **INTERNET\_MAX\_URL\_LENGTH**.</span></span>

</dd> <dt>

<span data-ttu-id="6cce9-112">*ppwszFileURL* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6cce9-112">*ppwszFileURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cce9-113">Recebe uma cadeia de caracteres terminada em nulo que contém a URL.</span><span class="sxs-lookup"><span data-stu-id="6cce9-113">Receives a null-terminated string that contains the URL.</span></span> <span data-ttu-id="6cce9-114">O chamador deve liberar a cadeia de caracteres chamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="6cce9-114">The caller must free the string by calling [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cce9-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cce9-115">Return value</span></span>

<span data-ttu-id="6cce9-116">A função retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6cce9-116">The function returns an **HRESULT**.</span></span> <span data-ttu-id="6cce9-117">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6cce9-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6cce9-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6cce9-118">Return code</span></span>                                                                             | <span data-ttu-id="6cce9-119">Description</span><span class="sxs-lookup"><span data-stu-id="6cce9-119">Description</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6cce9-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="6cce9-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6cce9-121">A cadeia de caracteres fornecida no parâmetro *pwszFilePath* já está no formato de URL.</span><span class="sxs-lookup"><span data-stu-id="6cce9-121">The string given in the *pwszFilePath* parameter is already in URL format.</span></span> <span data-ttu-id="6cce9-122">Nesse caso, *pszFilePath* é simplesmente copiado para *ppszFileURL* sem modificação.</span><span class="sxs-lookup"><span data-stu-id="6cce9-122">In this case, *pszFilePath* is simply copied to *ppszFileURL* without modification.</span></span><br/> |
| <dl> <span data-ttu-id="6cce9-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6cce9-123"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6cce9-124">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6cce9-124">The function succeeded.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="6cce9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cce9-125">Remarks</span></span>

<span data-ttu-id="6cce9-126">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="6cce9-126">This function has no associated import library.</span></span> <span data-ttu-id="6cce9-127">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mfplat.dll.</span><span class="sxs-lookup"><span data-stu-id="6cce9-127">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mfplat.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cce9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cce9-128">Requirements</span></span>



| <span data-ttu-id="6cce9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cce9-129">Requirement</span></span> | <span data-ttu-id="6cce9-130">Valor</span><span class="sxs-lookup"><span data-stu-id="6cce9-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cce9-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cce9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6cce9-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cce9-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cce9-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cce9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6cce9-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6cce9-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cce9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6cce9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cce9-136"><dt>Mfplat.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cce9-136"><dt>Mfplat.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cce9-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cce9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cce9-138">Funções de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6cce9-138">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
