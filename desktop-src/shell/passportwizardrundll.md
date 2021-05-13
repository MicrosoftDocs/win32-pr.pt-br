---
description: Inicia o assistente do Passport quando usado com Rundll32.exe.
title: Função PassportWizardRunDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: 1678677bcb305b7e5c47d28f5168d1e596ca3e26
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842507"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="b9979-103">Função PassportWizardRunDll</span><span class="sxs-lookup"><span data-stu-id="b9979-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="b9979-104">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b9979-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="b9979-105">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b9979-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b9979-106">Inicia o assistente do Passport quando usado com Rundll32.exe.</span><span class="sxs-lookup"><span data-stu-id="b9979-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9979-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9979-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="b9979-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9979-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9979-109">*hwndStub* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9979-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9979-110">Digite: **HWND**</span><span class="sxs-lookup"><span data-stu-id="b9979-110">Type: **HWND**</span></span>

<span data-ttu-id="b9979-111">Um identificador para uma janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="b9979-111">A handle to an owner window.</span></span> <span data-ttu-id="b9979-112">Esse parâmetro é normalmente definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b9979-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b9979-113">*hAppInstance* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9979-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9979-114">Tipo: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="b9979-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="b9979-115">Um identificador para o arquivo de biblioteca, obtido como um valor de retorno de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span><span class="sxs-lookup"><span data-stu-id="b9979-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="b9979-116">*lpszCmdLine* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9979-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9979-117">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="b9979-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="b9979-118">Dados de argumento.</span><span class="sxs-lookup"><span data-stu-id="b9979-118">Argument data.</span></span> <span data-ttu-id="b9979-119">Esse valor sempre estará vazio.</span><span class="sxs-lookup"><span data-stu-id="b9979-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="b9979-120">*nCmdShow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b9979-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9979-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b9979-121">Type: **int**</span></span>

<span data-ttu-id="b9979-122">Define o modo de exibição para a janela.</span><span class="sxs-lookup"><span data-stu-id="b9979-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9979-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9979-123">Return value</span></span>

<span data-ttu-id="b9979-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b9979-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9979-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9979-125">Remarks</span></span>

<span data-ttu-id="b9979-126">O assistente do Passport é usado para obter um Passport padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="b9979-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="b9979-127">Um Passport fornece ao usuário acesso personalizado a todos os sites do MSN e outros sites habilitados para Passport usando o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="b9979-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="b9979-128">Usar **PassportWizardRunDll** como um ponto de entrada no arquivo Netplwiz.dll por meio de um comando Rundll32 permite que você iniciar o Assistente do Passport em uma linha de comando como se fosse um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="b9979-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="b9979-129">**PassportWizardRunDll** é usado exclusivamente no contexto de um Rundll32.exe comando da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b9979-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="b9979-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span><span class="sxs-lookup"><span data-stu-id="b9979-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="b9979-131">Usar uma função de ponto de entrada com Rundll32.exe não se parece com uma chamada de função normal.</span><span class="sxs-lookup"><span data-stu-id="b9979-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="b9979-132">O nome da função e o nome do arquivo .dll em que ele está armazenado são usados apenas como parâmetros de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b9979-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="b9979-133">A definição de função mostrada em Sintaxe é apenas um protótipo padrão para todas as funções que você pode chamar usando Rundll32.</span><span class="sxs-lookup"><span data-stu-id="b9979-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="b9979-134">Os valores específicos para *hwndStub,* *hAppInstance* e *nCmdShow* não são fornecidos pelo usuário, mas são tratados em segundo plano pelo Rundll32.</span><span class="sxs-lookup"><span data-stu-id="b9979-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="b9979-135">**PassportWizardRunDll** não usa o valor *lpszCmdLine,* portanto, nenhum dado adicional é necessário.</span><span class="sxs-lookup"><span data-stu-id="b9979-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9979-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9979-136">Requirements</span></span>



| <span data-ttu-id="b9979-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9979-137">Requirement</span></span> | <span data-ttu-id="b9979-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b9979-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9979-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9979-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b9979-140">Somente \[ aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b9979-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="b9979-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9979-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b9979-142">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9979-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b9979-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9979-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9979-144"><dt>Nenhum</dt></span><span class="sxs-lookup"><span data-stu-id="b9979-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="b9979-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b9979-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9979-146"><dt>Netplwiz.dll (versão 5.60 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b9979-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
