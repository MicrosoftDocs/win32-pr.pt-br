---
title: Função SaveDefaultUserInputSettings
description: Aplica o layout de teclado do usuário e a configuração de serviço de texto ao hive do usuário padrão.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- Estrutura de serviços de texto da função SaveDefaultUserInputSettings
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369404"
---
# <a name="savedefaultuserinputsettings-function"></a><span data-ttu-id="97827-104">Função SaveDefaultUserInputSettings</span><span class="sxs-lookup"><span data-stu-id="97827-104">SaveDefaultUserInputSettings function</span></span>

<span data-ttu-id="97827-105">Aplica o layout de teclado do usuário e a configuração de serviço de texto ao hive do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="97827-105">Applies the user keyboard layout and text service setting to the default user hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="97827-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97827-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="97827-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97827-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97827-108">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97827-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97827-109">A janela pai da caixa de diálogo de aviso.</span><span class="sxs-lookup"><span data-stu-id="97827-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="97827-110">A caixa de diálogo de aviso nem sempre é mostrada e aparece adequadamente.</span><span class="sxs-lookup"><span data-stu-id="97827-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="97827-111">Se esse parâmetro for nulo, a caixa de diálogo de aviso não será mostrada.</span><span class="sxs-lookup"><span data-stu-id="97827-111">If this parameter is NULL, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="97827-112">*hSourceRegKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97827-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97827-113">A chave do registro raiz da configuração do usuário a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="97827-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97827-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97827-114">Return value</span></span>



| <span data-ttu-id="97827-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="97827-115">Return code</span></span>                                                                          | <span data-ttu-id="97827-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="97827-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="97827-117"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="97827-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="97827-118">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="97827-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="97827-119"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="97827-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="97827-120">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="97827-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="97827-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97827-121">Examples</span></span>

<span data-ttu-id="97827-122">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="97827-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="97827-123">O exemplo a seguir demonstra como obter um ponteiro para essa função.</span><span class="sxs-lookup"><span data-stu-id="97827-123">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="97827-124">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="97827-124">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="97827-125">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="97827-125">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="97827-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97827-126">Requirements</span></span>



| <span data-ttu-id="97827-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="97827-127">Requirement</span></span> | <span data-ttu-id="97827-128">Valor</span><span class="sxs-lookup"><span data-stu-id="97827-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97827-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97827-129">Minimum supported client</span></span><br/> | <span data-ttu-id="97827-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97827-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="97827-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97827-131">Minimum supported server</span></span><br/> | <span data-ttu-id="97827-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97827-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="97827-133">DLL</span><span class="sxs-lookup"><span data-stu-id="97827-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97827-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97827-134"><dt>Input.dll</dt></span></span> </dl> |



 

