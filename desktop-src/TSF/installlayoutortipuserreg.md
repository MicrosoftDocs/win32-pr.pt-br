---
title: Função InstallLayoutOrTipUserReg
description: Habilita os layouts de teclado ou os serviços de texto especificados para o usuário especificado.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Estrutura de serviços de texto da função InstallLayoutOrTipUserReg
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644681"
---
# <a name="installlayoutortipuserreg-function"></a><span data-ttu-id="0e872-104">Função InstallLayoutOrTipUserReg</span><span class="sxs-lookup"><span data-stu-id="0e872-104">InstallLayoutOrTipUserReg function</span></span>

<span data-ttu-id="0e872-105">Habilita os layouts de teclado ou os serviços de texto especificados para o usuário especificado.</span><span class="sxs-lookup"><span data-stu-id="0e872-105">Enables the specified keyboard layouts or text services for the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e872-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e872-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0e872-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e872-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e872-108">*pszUserReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0e872-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e872-109">O caminho do registro do usuário.</span><span class="sxs-lookup"><span data-stu-id="0e872-109">The registry path of the user.</span></span> <span data-ttu-id="0e872-110">Se esse parâmetro for **NULL**, hKey \_ Current \_ User será usado.</span><span class="sxs-lookup"><span data-stu-id="0e872-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="0e872-111">*pszSystemReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0e872-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e872-112">O caminho do registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="0e872-112">The registry path of the system.</span></span> <span data-ttu-id="0e872-113">Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ System será usado.</span><span class="sxs-lookup"><span data-stu-id="0e872-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="0e872-114">*pszSoftwareReg* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0e872-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e872-115">O caminho do registro do software.</span><span class="sxs-lookup"><span data-stu-id="0e872-115">The registry path of the software.</span></span> <span data-ttu-id="0e872-116">Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ software será usado.</span><span class="sxs-lookup"><span data-stu-id="0e872-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="0e872-117">*psz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e872-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e872-118">Uma cadeia de caracteres que representa a lista de layout do teclado ou a lista de perfis de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="0e872-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="0e872-119">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e872-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e872-120">Um campo de bits que especifica os sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e872-120">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="0e872-121">Os identificadores a seguir não estão definidos em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="0e872-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="0e872-122">Você deve usar o valor hexadecimal ou \# definir os identificadores.</span><span class="sxs-lookup"><span data-stu-id="0e872-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="0e872-123">Por exemplo, para usar **a \_ desinstalação do ILOT** , você deve incluir `#define ILOT_UNINSTALL 0x00000001` em seu código.</span><span class="sxs-lookup"><span data-stu-id="0e872-123">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="0e872-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0e872-124">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="0e872-125">Significado</span><span class="sxs-lookup"><span data-stu-id="0e872-125">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="0e872-126"><dt>**ILOT \_ DESINSTALAR**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0e872-126"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="0e872-127">O mesmo que **ILOT \_ desabilitado**.</span><span class="sxs-lookup"><span data-stu-id="0e872-127">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="0e872-128"><dt>**ILOT \_ DEFPROFILE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="0e872-128"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="0e872-129">Define o layout ou a dica especificado como um item padrão.</span><span class="sxs-lookup"><span data-stu-id="0e872-129">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="0e872-130"><dt>**ILOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="0e872-130"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="0e872-131">A configuração é salva, mas não é aplicada à sessão atual.</span><span class="sxs-lookup"><span data-stu-id="0e872-131">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="0e872-132"><dt>**ILOT \_ CLEANINSTALL**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="0e872-132"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="0e872-133">Desabilita todos os layouts de teclado e serviços de texto atuais.</span><span class="sxs-lookup"><span data-stu-id="0e872-133">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="0e872-134"><dt>**ILOT \_ 0x00000080 DESABILITAdo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0e872-134"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="0e872-135">Desabilita o layout de teclado e o serviço de texto especificados.</span><span class="sxs-lookup"><span data-stu-id="0e872-135">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e872-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e872-136">Return value</span></span>



| <span data-ttu-id="0e872-137">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0e872-137">Return code</span></span>                                                                         | <span data-ttu-id="0e872-138">Description</span><span class="sxs-lookup"><span data-stu-id="0e872-138">Description</span></span>                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0e872-139"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="0e872-139"><dt>**TRUE**</dt></span></span> </dl> | <span data-ttu-id="0e872-140">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0e872-140">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="0e872-141"><dt>**FASE**</dt></span><span class="sxs-lookup"><span data-stu-id="0e872-141"><dt>**FASE**</dt></span></span> </dl> | <span data-ttu-id="0e872-142">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="0e872-142">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e872-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e872-143">Remarks</span></span>

<span data-ttu-id="0e872-144">O formato da cadeia de caracteres da lista de layouts é:</span><span class="sxs-lookup"><span data-stu-id="0e872-144">The string format of the layout list is:</span></span>

<span data-ttu-id="0e872-145"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="0e872-145"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="0e872-146">O formato de cadeia de caracteres da lista de perfis de serviço de texto é:</span><span class="sxs-lookup"><span data-stu-id="0e872-146">The string format of the text service profile list is:</span></span>

<span data-ttu-id="0e872-147"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="0e872-147"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="0e872-148">Veja a seguir um exemplo de um valor para o parâmetro *psz* :</span><span class="sxs-lookup"><span data-stu-id="0e872-148">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="0e872-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e872-149">Examples</span></span>

<span data-ttu-id="0e872-150">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="0e872-150">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="0e872-151">O exemplo a seguir demonstra como obter um ponteiro para essa função.</span><span class="sxs-lookup"><span data-stu-id="0e872-151">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="0e872-152">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="0e872-152">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="0e872-153">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0e872-153">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="0e872-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e872-154">Requirements</span></span>



| <span data-ttu-id="0e872-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e872-155">Requirement</span></span> | <span data-ttu-id="0e872-156">Valor</span><span class="sxs-lookup"><span data-stu-id="0e872-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0e872-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e872-157">Minimum supported client</span></span><br/> | <span data-ttu-id="0e872-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e872-158">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0e872-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e872-159">Minimum supported server</span></span><br/> | <span data-ttu-id="0e872-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0e872-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0e872-161">DLL</span><span class="sxs-lookup"><span data-stu-id="0e872-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e872-162"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e872-162"><dt>Input.dll</dt></span></span> </dl> |



 

