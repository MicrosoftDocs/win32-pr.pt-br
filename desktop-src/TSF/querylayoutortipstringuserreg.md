---
title: Função QueryLayoutOrTipStringUserReg
description: Consulta a cadeia de caracteres especificada que representa o formato de uma lista de layout de teclado ou de perfil de serviços de texto do caminho do registro especificado.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- Estrutura de serviços de texto da função QueryLayoutOrTipStringUserReg
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779913"
---
# <a name="querylayoutortipstringuserreg-function"></a><span data-ttu-id="93127-104">Função QueryLayoutOrTipStringUserReg</span><span class="sxs-lookup"><span data-stu-id="93127-104">QueryLayoutOrTipStringUserReg function</span></span>

<span data-ttu-id="93127-105">Consulta a cadeia de caracteres especificada que representa o formato de uma lista de layout de teclado ou de perfil de serviços de texto do caminho do registro especificado.</span><span class="sxs-lookup"><span data-stu-id="93127-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list of the specified registry path.</span></span>

## <a name="syntax"></a><span data-ttu-id="93127-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93127-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="93127-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93127-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93127-108">*pszUserReg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93127-108">*pszUserReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93127-109">O caminho do registro do usuário.</span><span class="sxs-lookup"><span data-stu-id="93127-109">The registry path of the user.</span></span> <span data-ttu-id="93127-110">Se esse parâmetro for **NULL**, hKey \_ Current \_ User será usado.</span><span class="sxs-lookup"><span data-stu-id="93127-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="93127-111">*pszSystemReg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93127-111">*pszSystemReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93127-112">O caminho do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="93127-112">The registry path of the system.</span></span> <span data-ttu-id="93127-113">Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ System será usado.</span><span class="sxs-lookup"><span data-stu-id="93127-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="93127-114">*pszSoftwareReg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93127-114">*pszSoftwareReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93127-115">O caminho do registro do software.</span><span class="sxs-lookup"><span data-stu-id="93127-115">The registry path of the software.</span></span> <span data-ttu-id="93127-116">Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ software será usado.</span><span class="sxs-lookup"><span data-stu-id="93127-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="93127-117">*psz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93127-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93127-118">Uma cadeia de caracteres que representa uma lista de layout de teclado ou uma lista de perfis de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="93127-118">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="93127-119">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93127-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93127-120">Isso deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="93127-120">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93127-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93127-121">Return value</span></span>

<span data-ttu-id="93127-122">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="93127-122">This function can return one of these values.</span></span>



| <span data-ttu-id="93127-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="93127-123">Return code</span></span>                                                                                  | <span data-ttu-id="93127-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="93127-124">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93127-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="93127-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="93127-126">Todos os layouts ou perfis definidos em **psz** são válidos.</span><span class="sxs-lookup"><span data-stu-id="93127-126">All layouts or profiles defined in **psz** are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="93127-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="93127-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="93127-128">Um ou mais dos layouts ou perfis definidos em **psz** são inválidos.</span><span class="sxs-lookup"><span data-stu-id="93127-128">One or more of the layouts or profiles defined in **psz** are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93127-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="93127-129">Remarks</span></span>

<span data-ttu-id="93127-130">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="93127-130">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="93127-131">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="93127-131">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="93127-132">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="93127-132">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="93127-133">O formato da cadeia de caracteres da lista de layouts é:</span><span class="sxs-lookup"><span data-stu-id="93127-133">The string format of the layout list is:</span></span>

<span data-ttu-id="93127-134"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="93127-134"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="93127-135">O formato de cadeia de caracteres da lista de perfis de serviço de texto é:</span><span class="sxs-lookup"><span data-stu-id="93127-135">The string format of the text service profile list is:</span></span>

<span data-ttu-id="93127-136"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="93127-136"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="93127-137">Veja a seguir um exemplo de um valor para o parâmetro *psz* :</span><span class="sxs-lookup"><span data-stu-id="93127-137">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="93127-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93127-138">Requirements</span></span>



| <span data-ttu-id="93127-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="93127-139">Requirement</span></span> | <span data-ttu-id="93127-140">Valor</span><span class="sxs-lookup"><span data-stu-id="93127-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93127-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93127-141">Minimum supported client</span></span><br/> | <span data-ttu-id="93127-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93127-142">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="93127-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93127-143">Minimum supported server</span></span><br/> | <span data-ttu-id="93127-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93127-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="93127-145">DLL</span><span class="sxs-lookup"><span data-stu-id="93127-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93127-146"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93127-146"><dt>Input.dll</dt></span></span> </dl> |



 

