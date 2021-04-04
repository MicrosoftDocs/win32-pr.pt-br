---
title: Função SetDefaultLayoutOrTip
description: Define o layout do teclado ou um serviço de texto especificado como o item de entrada padrão do usuário atual.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- Estrutura de serviços de texto da função SetDefaultLayoutOrTip
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085320"
---
# <a name="setdefaultlayoutortip-function"></a><span data-ttu-id="c1cf4-104">Função SetDefaultLayoutOrTip</span><span class="sxs-lookup"><span data-stu-id="c1cf4-104">SetDefaultLayoutOrTip function</span></span>

<span data-ttu-id="c1cf4-105">Define o layout do teclado ou um serviço de texto especificado como o item de entrada padrão do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-105">Sets the specified keyboard layout or a text service as the default input item of the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cf4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c1cf4-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c1cf4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1cf4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1cf4-108">*psz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1cf4-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cf4-109">Uma cadeia de caracteres que representa uma lista de layout de teclado ou uma lista de perfis de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="c1cf4-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c1cf4-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cf4-111">Um campo de bits que especifica os sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-111">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="c1cf4-112">Os identificadores a seguir não estão definidos em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="c1cf4-113">Você deve usar o valor hexadecimal ou \# definir os identificadores.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="c1cf4-114">Por exemplo, para usar SDLOT \_ NOAPPLYTOCURRENTSESSION, você deve incluir \# definir SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 em seu código.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-114">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="c1cf4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c1cf4-115">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="c1cf4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c1cf4-116">Meaning</span></span>                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="c1cf4-117"><dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c1cf4-117"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="c1cf4-118">Armazena a configuração no registro, mas dose não atualiza a configuração de teclado de tempo de execução da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-118">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="c1cf4-119">Se o caminho de registro alternativo for definido em [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), esse sinalizador deverá ser definido.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-119">If the alternative registry path is set in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="c1cf4-120"><dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="c1cf4-120"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="c1cf4-121">Aplica a configuração imediatamente no thread atual.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-121">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1cf4-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1cf4-122">Return value</span></span>



| <span data-ttu-id="c1cf4-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c1cf4-123">Return code</span></span>                                                                          | <span data-ttu-id="c1cf4-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1cf4-124">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="c1cf4-125"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="c1cf4-125"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="c1cf4-126">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-126">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="c1cf4-127"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="c1cf4-127"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="c1cf4-128">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-128">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c1cf4-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1cf4-129">Remarks</span></span>

<span data-ttu-id="c1cf4-130">O formato da cadeia de caracteres da lista de layouts é:</span><span class="sxs-lookup"><span data-stu-id="c1cf4-130">The string format of the layout list is:</span></span>

<span data-ttu-id="c1cf4-131"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="c1cf4-131"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="c1cf4-132">O formato de cadeia de caracteres da lista de perfis de serviço de texto é:</span><span class="sxs-lookup"><span data-stu-id="c1cf4-132">The string format of the text service profile list is:</span></span>

<span data-ttu-id="c1cf4-133"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="c1cf4-133"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="c1cf4-134">Veja a seguir um exemplo de um valor para o parâmetro *psz* :</span><span class="sxs-lookup"><span data-stu-id="c1cf4-134">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="c1cf4-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c1cf4-135">Examples</span></span>

<span data-ttu-id="c1cf4-136">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="c1cf4-136">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="c1cf4-137">O exemplo a seguir demonstra como obter um ponteiro para essa função.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-137">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="c1cf4-138">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-138">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="c1cf4-139">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c1cf4-139">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="c1cf4-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1cf4-140">Requirements</span></span>



| <span data-ttu-id="c1cf4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1cf4-141">Requirement</span></span> | <span data-ttu-id="c1cf4-142">Valor</span><span class="sxs-lookup"><span data-stu-id="c1cf4-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cf4-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1cf4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cf4-144">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1cf4-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c1cf4-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1cf4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cf4-146">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1cf4-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c1cf4-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c1cf4-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1cf4-148"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1cf4-148"><dt>Input.dll</dt></span></span> </dl> |



 

