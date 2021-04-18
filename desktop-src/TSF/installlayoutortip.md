---
title: Função InstallLayoutOrTip
description: Habilita os layouts de teclado ou os serviços de texto especificados.
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- Estrutura de serviços de texto da função InstallLayoutOrTip
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788074"
---
# <a name="installlayoutortip-function"></a><span data-ttu-id="1dcd9-104">Função InstallLayoutOrTip</span><span class="sxs-lookup"><span data-stu-id="1dcd9-104">InstallLayoutOrTip function</span></span>

<span data-ttu-id="1dcd9-105">Habilita os layouts de teclado ou os serviços de texto especificados.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-105">Enables the specified keyboard layouts or text services.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dcd9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1dcd9-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1dcd9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dcd9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dcd9-108">*psz* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1dcd9-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcd9-109">Uma cadeia de caracteres que representa a lista de layout do teclado ou a lista de perfis de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-109">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="1dcd9-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1dcd9-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dcd9-111">Um campo de bits que especifica os seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="1dcd9-111">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="1dcd9-112">Os identificadores a seguir não estão definidos em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="1dcd9-113">Você deve usar o valor hexadecimal ou \# definir os identificadores.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="1dcd9-114">Por exemplo, para usar **a \_ desinstalação do ILOT** , você deve incluir `#define ILOT_UNINSTALL 0x00000001` em seu código.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-114">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="1dcd9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1dcd9-115">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="1dcd9-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1dcd9-116">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="1dcd9-117"><dt>**ILOT \_ DESINSTALAR**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-117"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="1dcd9-118">O mesmo que **ILOT \_ desabilitado**.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-118">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="1dcd9-119"><dt>**ILOT \_ DEFPROFILE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-119"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="1dcd9-120">Define o layout ou a dica especificado como um item padrão.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-120">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <span data-ttu-id="1dcd9-121"><dt>**ILOT \_ DEFUSER4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-121"><dt>**ILOT\_DEFUSER4**</dt> <dt>0x00000004</dt></span></span> </dl>                                              | <span data-ttu-id="1dcd9-122">Altera a configuração de. Os.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-122">Changes the setting of .Default.</span></span><br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <span data-ttu-id="1dcd9-123"><dt>**ILOT \_ SYSLOCALE**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-123"><dt>**ILOT\_SYSLOCALE**</dt> <dt>0x00000008</dt></span></span> </dl>                                           | <span data-ttu-id="1dcd9-124">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-124">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <span data-ttu-id="1dcd9-125"><dt>**ILOT \_ NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-125"><dt>**ILOT\_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="1dcd9-126">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-126">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="1dcd9-127"><dt>**ILOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-127"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="1dcd9-128">A configuração é salva, mas não é aplicada à sessão atual.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-128">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="1dcd9-129"><dt>**ILOT \_ CLEANINSTALL**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-129"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="1dcd9-130">Desabilita todos os layouts de teclado e serviços de texto atuais.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-130">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="1dcd9-131"><dt>**ILOT \_ 0x00000080 DESABILITAdo**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-131"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="1dcd9-132">Desabilita o layout de teclado e o serviço de texto especificados.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-132">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dcd9-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1dcd9-133">Return value</span></span>



| <span data-ttu-id="1dcd9-134">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1dcd9-134">Return code</span></span>                                                                          | <span data-ttu-id="1dcd9-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="1dcd9-135">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="1dcd9-136"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-136"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="1dcd9-137">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-137">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="1dcd9-138"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-138"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="1dcd9-139">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-139">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1dcd9-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dcd9-140">Remarks</span></span>

<span data-ttu-id="1dcd9-141">O formato da cadeia de caracteres da lista de layouts é:</span><span class="sxs-lookup"><span data-stu-id="1dcd9-141">The string format of the layout list is:</span></span>

<span data-ttu-id="1dcd9-142"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="1dcd9-142"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="1dcd9-143">O formato de cadeia de caracteres da lista de perfis de serviço de texto é:</span><span class="sxs-lookup"><span data-stu-id="1dcd9-143">The string format of the text service profile list is:</span></span>

<span data-ttu-id="1dcd9-144"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="1dcd9-144"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="1dcd9-145">Veja a seguir um exemplo de um valor para o parâmetro *psz* :</span><span class="sxs-lookup"><span data-stu-id="1dcd9-145">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="1dcd9-146">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1dcd9-146">Examples</span></span>

<span data-ttu-id="1dcd9-147">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="1dcd9-147">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="1dcd9-148">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-148">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="1dcd9-149">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1dcd9-149">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="1dcd9-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dcd9-150">Requirements</span></span>



| <span data-ttu-id="1dcd9-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dcd9-151">Requirement</span></span> | <span data-ttu-id="1dcd9-152">Valor</span><span class="sxs-lookup"><span data-stu-id="1dcd9-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1dcd9-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dcd9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="1dcd9-154">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1dcd9-154">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1dcd9-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1dcd9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="1dcd9-156">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1dcd9-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1dcd9-157">DLL</span><span class="sxs-lookup"><span data-stu-id="1dcd9-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dcd9-158"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dcd9-158"><dt>Input.dll</dt></span></span> </dl> |



 

