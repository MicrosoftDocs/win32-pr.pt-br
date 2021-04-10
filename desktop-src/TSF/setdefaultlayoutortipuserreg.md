---
title: Função SetDefaultLayoutOrTipUserReg
description: Define o layout do teclado especificado ou um serviço de texto como um item de entrada padrão do registro do usuário.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- Estrutura de serviços de texto da função SetDefaultLayoutOrTipUserReg
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085232"
---
# <a name="setdefaultlayoutortipuserreg-function"></a><span data-ttu-id="303cb-104">Função SetDefaultLayoutOrTipUserReg</span><span class="sxs-lookup"><span data-stu-id="303cb-104">SetDefaultLayoutOrTipUserReg function</span></span>

<span data-ttu-id="303cb-105">Define o layout do teclado especificado ou um serviço de texto como um item de entrada padrão do registro do usuário.</span><span class="sxs-lookup"><span data-stu-id="303cb-105">Sets the specified keyboard layout or a text service as a default input item of the user registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="303cb-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="303cb-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="303cb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="303cb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303cb-108">*pszUserReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="303cb-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="303cb-109">O caminho do registro do usuário.</span><span class="sxs-lookup"><span data-stu-id="303cb-109">The registry path of the user.</span></span> <span data-ttu-id="303cb-110">Se esse parâmetro for **NULL**, hKey \_ Current \_ User será usado.</span><span class="sxs-lookup"><span data-stu-id="303cb-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="303cb-111">*pszSystemReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="303cb-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="303cb-112">O caminho do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="303cb-112">The registry path of the system.</span></span> <span data-ttu-id="303cb-113">Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ System será usado.</span><span class="sxs-lookup"><span data-stu-id="303cb-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="303cb-114">*pszSoftwareReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="303cb-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="303cb-115">O caminho do registro do software.</span><span class="sxs-lookup"><span data-stu-id="303cb-115">The registry path of the software.</span></span> <span data-ttu-id="303cb-116">Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ software será usado.</span><span class="sxs-lookup"><span data-stu-id="303cb-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="303cb-117">*psz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="303cb-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303cb-118">Uma cadeia de caracteres que representa a lista de layout do teclado ou a lista de perfis de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="303cb-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="303cb-119">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="303cb-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303cb-120">Um campo de bits que especifica os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="303cb-120">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="303cb-121">Os identificadores a seguir não estão definidos em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="303cb-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="303cb-122">Você deve usar o valor hexadecimal ou \# definir os identificadores.</span><span class="sxs-lookup"><span data-stu-id="303cb-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="303cb-123">Por exemplo, para usar SDLOT \_ NOAPPLYTOCURRENTSESSION, você deve incluir \# definir SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 em seu código.</span><span class="sxs-lookup"><span data-stu-id="303cb-123">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="303cb-124">Valor</span><span class="sxs-lookup"><span data-stu-id="303cb-124">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="303cb-125">Significado</span><span class="sxs-lookup"><span data-stu-id="303cb-125">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="303cb-126"><dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="303cb-126"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="303cb-127">Armazena a configuração no registro, mas dose não atualiza a configuração de teclado de tempo de execução da sessão atual.</span><span class="sxs-lookup"><span data-stu-id="303cb-127">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="303cb-128">Se o caminho de registro alternativo for definido em **SetDefaultLayoutOrTipUserReg**, esse sinalizador deverá ser definido.</span><span class="sxs-lookup"><span data-stu-id="303cb-128">If the alternative registry path is set in **SetDefaultLayoutOrTipUserReg**, this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="303cb-129"><dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="303cb-129"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="303cb-130">Aplica a configuração imediatamente no thread atual.</span><span class="sxs-lookup"><span data-stu-id="303cb-130">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303cb-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="303cb-131">Return value</span></span>



| <span data-ttu-id="303cb-132">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="303cb-132">Return code</span></span>                                                                          | <span data-ttu-id="303cb-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="303cb-133">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="303cb-134"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="303cb-134"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="303cb-135">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="303cb-135">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="303cb-136"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="303cb-136"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="303cb-137">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="303cb-137">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="303cb-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="303cb-138">Remarks</span></span>

<span data-ttu-id="303cb-139">O formato da cadeia de caracteres da lista de layouts é:</span><span class="sxs-lookup"><span data-stu-id="303cb-139">The string format of the layout list is:</span></span>

<span data-ttu-id="303cb-140"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="303cb-140"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="303cb-141">O formato de cadeia de caracteres da lista de perfis de serviço de texto é:</span><span class="sxs-lookup"><span data-stu-id="303cb-141">The string format of the text service profile list is:</span></span>

<span data-ttu-id="303cb-142"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="303cb-142"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="303cb-143">Veja a seguir um exemplo de um valor para o parâmetro *psz* :</span><span class="sxs-lookup"><span data-stu-id="303cb-143">The following is an example of a value for the *psz* parameter:</span></span>


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="303cb-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="303cb-144">Examples</span></span>

<span data-ttu-id="303cb-145">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="303cb-145">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="303cb-146">O exemplo a seguir demonstra como obter um ponteiro para essa função.</span><span class="sxs-lookup"><span data-stu-id="303cb-146">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="303cb-147">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="303cb-147">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="303cb-148">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="303cb-148">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="303cb-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="303cb-149">Requirements</span></span>



| <span data-ttu-id="303cb-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="303cb-150">Requirement</span></span> | <span data-ttu-id="303cb-151">Valor</span><span class="sxs-lookup"><span data-stu-id="303cb-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="303cb-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="303cb-152">Minimum supported client</span></span><br/> | <span data-ttu-id="303cb-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="303cb-153">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="303cb-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="303cb-154">Minimum supported server</span></span><br/> | <span data-ttu-id="303cb-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="303cb-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="303cb-156">DLL</span><span class="sxs-lookup"><span data-stu-id="303cb-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="303cb-157"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="303cb-157"><dt>Input.dll</dt></span></span> </dl> |



 

