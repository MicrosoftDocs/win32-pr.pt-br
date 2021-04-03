---
description: A função AdvancedDocumentProperties exibe uma caixa de diálogo de configuração de impressora para a impressora especificada, permitindo que o usuário configure essa impressora.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Função AdvancedDocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663175"
---
# <a name="advanceddocumentproperties-function"></a><span data-ttu-id="321c2-103">Função AdvancedDocumentProperties</span><span class="sxs-lookup"><span data-stu-id="321c2-103">AdvancedDocumentProperties function</span></span>

<span data-ttu-id="321c2-104">A função **AdvancedDocumentProperties** exibe uma caixa de diálogo de configuração de impressora para a impressora especificada, permitindo que o usuário configure essa impressora.</span><span class="sxs-lookup"><span data-stu-id="321c2-104">The **AdvancedDocumentProperties** function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.</span></span>

<span data-ttu-id="321c2-105">Essa função é um caso especial da função [**DocumentProperties**](documentproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="321c2-105">This function is a special case of the [**DocumentProperties**](documentproperties.md) function.</span></span> <span data-ttu-id="321c2-106">Para obter mais detalhes, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="321c2-106">For more details, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="321c2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="321c2-107">Syntax</span></span>


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a><span data-ttu-id="321c2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="321c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="321c2-109">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="321c2-109">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="321c2-110">Um identificador para a janela pai da caixa de diálogo de configuração da impressora.</span><span class="sxs-lookup"><span data-stu-id="321c2-110">A handle to the parent window of the printer-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="321c2-111">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="321c2-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="321c2-112">Um identificador para um objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="321c2-112">A handle to a printer object.</span></span> <span data-ttu-id="321c2-113">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="321c2-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="321c2-114">*pDeviceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="321c2-114">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="321c2-115">Um ponteiro para uma cadeia de caracteres terminada em nulo especificando o nome do dispositivo para o qual uma caixa de diálogo de configuração de impressora deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="321c2-115">A pointer to a null-terminated string specifying the name of the device for which a printer-configuration dialog box should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="321c2-116">*pDevModeOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="321c2-116">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="321c2-117">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que conterá os dados de configuração especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="321c2-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that will contain the configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="321c2-118">*pDevModeInput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="321c2-118">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="321c2-119">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contém os dados de configuração usados para inicializar os controles da caixa de diálogo configuração da impressora.</span><span class="sxs-lookup"><span data-stu-id="321c2-119">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains the configuration data used to initialize the controls of the printer-configuration dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="321c2-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="321c2-120">Return value</span></span>

<span data-ttu-id="321c2-121">Se a função [**DocumentProperties**](documentproperties.md) com esses parâmetros for bem-sucedida, o valor de retorno de **AdvancedDocumentProperties** será 1.</span><span class="sxs-lookup"><span data-stu-id="321c2-121">If the [**DocumentProperties**](documentproperties.md) function with these parameters is successful, the return value of **AdvancedDocumentProperties** is 1.</span></span> <span data-ttu-id="321c2-122">Caso contrário, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="321c2-122">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="321c2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="321c2-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="321c2-124">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="321c2-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="321c2-125">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="321c2-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="321c2-126">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="321c2-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="321c2-127">Essa função só pode exibir a caixa de diálogo configuração da impressora para que um usuário possa configurá-la.</span><span class="sxs-lookup"><span data-stu-id="321c2-127">This function can only display the printer-configuration dialog box so a user can configure it.</span></span> <span data-ttu-id="321c2-128">Para obter mais controle, use [**DocumentProperties**](documentproperties.md).</span><span class="sxs-lookup"><span data-stu-id="321c2-128">For more control, use [**DocumentProperties**](documentproperties.md).</span></span> <span data-ttu-id="321c2-129">Os parâmetros de entrada para essa função são passados diretamente para **DocumentProperties** e o valor de *fMode* é definido como DM \_ no \_ buffer \| DM \_ no \_ prompt \| DM \_ out \_ buffer.</span><span class="sxs-lookup"><span data-stu-id="321c2-129">The input parameters for this function are passed directly to **DocumentProperties** and the *fMode* value is set to DM\_IN\_BUFFER \| DM\_IN\_PROMPT \| DM\_OUT\_BUFFER.</span></span> <span data-ttu-id="321c2-130">Ao contrário de **DocumentProperties**, essa função retorna apenas 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="321c2-130">Unlike **DocumentProperties**, this function only returns 1 or 0.</span></span> <span data-ttu-id="321c2-131">Portanto, você não pode determinar o tamanho necessário de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definindo *pDevMode* como zero.</span><span class="sxs-lookup"><span data-stu-id="321c2-131">Thus, you cannot determine the required size of [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) by setting *pDevMode* to zero.</span></span>

<span data-ttu-id="321c2-132">Um aplicativo pode obter o nome apontado pelo parâmetro *pDeviceName* chamando a função [**getprinter**](getprinter.md) e, em seguida, examinando o membro **pPrinterName** da estrutura [**\_ info \_ 2 da impressora**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="321c2-132">An application can obtain the name pointed to by the *pDeviceName* parameter by calling the [**GetPrinter**](getprinter.md) function and then examining the **pPrinterName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="321c2-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="321c2-133">Requirements</span></span>



| <span data-ttu-id="321c2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="321c2-134">Requirement</span></span> | <span data-ttu-id="321c2-135">Valor</span><span class="sxs-lookup"><span data-stu-id="321c2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="321c2-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="321c2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="321c2-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="321c2-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="321c2-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="321c2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="321c2-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="321c2-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="321c2-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="321c2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="321c2-141"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="321c2-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="321c2-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="321c2-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="321c2-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="321c2-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="321c2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="321c2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="321c2-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="321c2-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="321c2-146">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="321c2-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="321c2-147">**AdvancedDocumentPropertiesW** (Unicode) e **AdvancedDocumentPropertiesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="321c2-147">**AdvancedDocumentPropertiesW** (Unicode) and **AdvancedDocumentPropertiesA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="321c2-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="321c2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321c2-149">Impressão</span><span class="sxs-lookup"><span data-stu-id="321c2-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="321c2-150">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="321c2-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="321c2-151">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="321c2-151">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="321c2-152">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="321c2-152">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="321c2-153">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="321c2-153">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="321c2-154">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="321c2-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="321c2-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="321c2-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="321c2-156">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="321c2-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




