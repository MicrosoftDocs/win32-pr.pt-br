---
title: Função SaveSystemAcctInputSettings
description: Aplica o layout de teclado do usuário e a configuração de serviço de texto ao hive de contas do sistema.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Estrutura de serviços de texto da função SaveSystemAcctInputSettings
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369272"
---
# <a name="savesystemacctinputsettings-function"></a><span data-ttu-id="84719-104">Função SaveSystemAcctInputSettings</span><span class="sxs-lookup"><span data-stu-id="84719-104">SaveSystemAcctInputSettings function</span></span>

<span data-ttu-id="84719-105">Aplica o layout de teclado do usuário e a configuração de serviço de texto ao hive de contas do sistema.</span><span class="sxs-lookup"><span data-stu-id="84719-105">Applies the user keyboard layout and text service setting to the system accounts hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="84719-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84719-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="84719-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84719-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84719-108">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84719-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84719-109">A janela pai da caixa de diálogo de aviso.</span><span class="sxs-lookup"><span data-stu-id="84719-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="84719-110">A caixa de diálogo de aviso nem sempre é mostrada e aparece adequadamente.</span><span class="sxs-lookup"><span data-stu-id="84719-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="84719-111">Se esse parâmetro for **nulo**, a caixa de diálogo de aviso não será mostrada.</span><span class="sxs-lookup"><span data-stu-id="84719-111">If this parameter is **NULL**, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="84719-112">*hSourceRegKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84719-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84719-113">A chave do registro raiz da configuração do usuário a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="84719-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84719-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84719-114">Return value</span></span>



| <span data-ttu-id="84719-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="84719-115">Return code</span></span>                                                                          | <span data-ttu-id="84719-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="84719-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="84719-117"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="84719-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="84719-118">A função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="84719-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="84719-119"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="84719-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="84719-120">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="84719-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84719-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="84719-121">Remarks</span></span>

<span data-ttu-id="84719-122">O hive da conta do sistema é o HKEY \_ Users \\ . PADRÃO, HKEY \_ Users \\ s-1-5-19 e hKey \_ Users \\ s-1-5-20.</span><span class="sxs-lookup"><span data-stu-id="84719-122">The system account hive is HKEY\_USERS\\.DEFAULT, HKEY\_USERS\\S-1-5-19, and HKEY\_USERS\\S-1-5-20.</span></span>

## <a name="examples"></a><span data-ttu-id="84719-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84719-123">Examples</span></span>

<span data-ttu-id="84719-124">Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="84719-124">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="84719-125">O exemplo a seguir demonstra como obter um ponteiro para essa função.</span><span class="sxs-lookup"><span data-stu-id="84719-125">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="84719-126">O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada.</span><span class="sxs-lookup"><span data-stu-id="84719-126">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="84719-127">Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="84719-127">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="84719-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84719-128">Requirements</span></span>



| <span data-ttu-id="84719-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="84719-129">Requirement</span></span> | <span data-ttu-id="84719-130">Valor</span><span class="sxs-lookup"><span data-stu-id="84719-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="84719-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84719-131">Minimum supported client</span></span><br/> | <span data-ttu-id="84719-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84719-132">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="84719-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84719-133">Minimum supported server</span></span><br/> | <span data-ttu-id="84719-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84719-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="84719-135">DLL</span><span class="sxs-lookup"><span data-stu-id="84719-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84719-136"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84719-136"><dt>Input.dll</dt></span></span> </dl> |



 

