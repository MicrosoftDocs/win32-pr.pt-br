---
title: Função QueryLayoutOrTipString
description: Consulta a cadeia de caracteres especificada que representa o formato de uma lista de layout de teclado ou de perfil de serviços de texto.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- Estrutura de serviços de texto da função QueryLayoutOrTipString
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784103"
---
# <a name="querylayoutortipstring-function"></a><span data-ttu-id="89370-104">Função QueryLayoutOrTipString</span><span class="sxs-lookup"><span data-stu-id="89370-104">QueryLayoutOrTipString function</span></span>

<span data-ttu-id="89370-105">Consulta a cadeia de caracteres especificada que representa o formato de uma lista de layout de teclado ou de perfil de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="89370-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list.</span></span>

## <a name="syntax"></a><span data-ttu-id="89370-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89370-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="89370-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89370-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89370-108">*psz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89370-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89370-109">Uma cadeia de caracteres que representa uma lista de layout de teclado ou uma lista de perfis de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="89370-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="89370-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89370-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89370-111">Isso deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="89370-111">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89370-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89370-112">Return value</span></span>

<span data-ttu-id="89370-113">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="89370-113">This function can return one of these values.</span></span>



| <span data-ttu-id="89370-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="89370-114">Return code</span></span>                                                                                  | <span data-ttu-id="89370-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="89370-115">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89370-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89370-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="89370-117">Todos os layouts ou perfis definidos em *psz* são válidos.</span><span class="sxs-lookup"><span data-stu-id="89370-117">All layouts or profiles defined in *psz* are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="89370-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="89370-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="89370-119">Um ou mais dos layouts ou perfis definidos em *psz* são inválidos.</span><span class="sxs-lookup"><span data-stu-id="89370-119">One or more of the layouts or profiles defined in *psz* are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89370-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="89370-120">Remarks</span></span>

<span data-ttu-id="89370-121">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="89370-121">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="89370-122">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="89370-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="89370-123">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="89370-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="89370-124">O formato da cadeia de caracteres da lista de layouts é:</span><span class="sxs-lookup"><span data-stu-id="89370-124">The string format of the layout list is:</span></span>

<span data-ttu-id="89370-125"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="89370-125"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="89370-126">O formato de cadeia de caracteres da lista de perfis de serviço de texto é:</span><span class="sxs-lookup"><span data-stu-id="89370-126">The string format of the text service profile list is:</span></span>

<span data-ttu-id="89370-127"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="89370-127"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="89370-128">Veja a seguir um exemplo de um valor para o parâmetro *psz* :</span><span class="sxs-lookup"><span data-stu-id="89370-128">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="89370-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89370-129">Requirements</span></span>



| <span data-ttu-id="89370-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="89370-130">Requirement</span></span> | <span data-ttu-id="89370-131">Valor</span><span class="sxs-lookup"><span data-stu-id="89370-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="89370-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89370-132">Minimum supported client</span></span><br/> | <span data-ttu-id="89370-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89370-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="89370-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89370-134">Minimum supported server</span></span><br/> | <span data-ttu-id="89370-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89370-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="89370-136">DLL</span><span class="sxs-lookup"><span data-stu-id="89370-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89370-137"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89370-137"><dt>Input.dll</dt></span></span> </dl> |



 

