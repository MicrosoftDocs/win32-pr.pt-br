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
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170094"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="0dfd9-103">Função PassportWizardRunDll</span><span class="sxs-lookup"><span data-stu-id="0dfd9-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="0dfd9-104">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="0dfd9-105">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0dfd9-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="0dfd9-106">Inicia o assistente do Passport quando usado com Rundll32.exe.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dfd9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0dfd9-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="0dfd9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0dfd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dfd9-109">*hwndStub* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0dfd9-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dfd9-110">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="0dfd9-110">Type: **HWND**</span></span>

<span data-ttu-id="0dfd9-111">Um identificador para uma janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-111">A handle to an owner window.</span></span> <span data-ttu-id="0dfd9-112">Esse parâmetro é normalmente definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0dfd9-113">*hAppInstance* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0dfd9-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dfd9-114">Tipo: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="0dfd9-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="0dfd9-115">Um identificador para o arquivo de biblioteca, obtido como um valor de retorno de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span><span class="sxs-lookup"><span data-stu-id="0dfd9-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="0dfd9-116">*lpszCmdLine* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0dfd9-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dfd9-117">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="0dfd9-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="0dfd9-118">Dados de argumento.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-118">Argument data.</span></span> <span data-ttu-id="0dfd9-119">Esse valor sempre estará vazio.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="0dfd9-120">*nCmdShow* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0dfd9-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dfd9-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0dfd9-121">Type: **int**</span></span>

<span data-ttu-id="0dfd9-122">Define o modo de exibição para a janela.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dfd9-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0dfd9-123">Return value</span></span>

<span data-ttu-id="0dfd9-124">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dfd9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dfd9-125">Remarks</span></span>

<span data-ttu-id="0dfd9-126">O assistente do Passport é usado para obter um Passport padrão do Windows.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="0dfd9-127">Um Passport fornece ao usuário acesso personalizado a todos os sites do MSN e outros sites habilitados para Passport usando o endereço de email do usuário.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="0dfd9-128">O uso de **PassportWizardRunDll** como um ponto de entrada no arquivo de Netplwiz.dll por meio de um comando rundll32 permite iniciar o assistente do Passport a partir de uma linha de comando como se fosse um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="0dfd9-129">**PassportWizardRunDll** é usado exclusivamente no contexto de um comando Rundll32.exe da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0dfd9-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="0dfd9-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span><span class="sxs-lookup"><span data-stu-id="0dfd9-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="0dfd9-131">O uso de uma função de ponto de entrada com Rundll32.exe não se assemelha a uma chamada de função normal.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="0dfd9-132">O nome da função e o nome do arquivo. dll onde ele está armazenado são usados apenas como parâmetros de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="0dfd9-133">A definição de função mostrada em sintaxe é apenas um protótipo padrão para todas as funções que você pode chamar usando rundll32.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="0dfd9-134">Os valores específicos para *hwndStub*, *hAppInstance* e *nCmdShow* não são fornecidos pelo usuário, mas são tratados em segundo plano por rundll32.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="0dfd9-135">**PassportWizardRunDll** não usa o valor *lpszCmdLine* , portanto, nenhum dado adicional é necessário.</span><span class="sxs-lookup"><span data-stu-id="0dfd9-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dfd9-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dfd9-136">Requirements</span></span>



| <span data-ttu-id="0dfd9-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dfd9-137">Requirement</span></span> | <span data-ttu-id="0dfd9-138">Valor</span><span class="sxs-lookup"><span data-stu-id="0dfd9-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dfd9-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dfd9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0dfd9-140">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0dfd9-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="0dfd9-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0dfd9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0dfd9-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0dfd9-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0dfd9-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0dfd9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dfd9-144"><dt>Nenhum</dt></span><span class="sxs-lookup"><span data-stu-id="0dfd9-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="0dfd9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0dfd9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dfd9-146"><dt>Netplwiz.dll (versão 5,60 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0dfd9-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
