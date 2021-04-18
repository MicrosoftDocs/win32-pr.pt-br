---
description: A função ConnectToPrinterDlg exibe uma caixa de diálogo que permite aos usuários navegar e se conectar a impressoras em uma rede.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Função ConnectToPrinterDlg (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810195"
---
# <a name="connecttoprinterdlg-function"></a><span data-ttu-id="c2267-103">Função ConnectToPrinterDlg</span><span class="sxs-lookup"><span data-stu-id="c2267-103">ConnectToPrinterDlg function</span></span>

<span data-ttu-id="c2267-104">A função **ConnectToPrinterDlg** exibe uma caixa de diálogo que permite aos usuários navegar e se conectar a impressoras em uma rede.</span><span class="sxs-lookup"><span data-stu-id="c2267-104">The **ConnectToPrinterDlg** function displays a dialog box that lets users browse and connect to printers on a network.</span></span> <span data-ttu-id="c2267-105">Se o usuário selecionar uma impressora, a função tentará criar uma conexão a ela; se um driver adequado não estiver instalado no servidor, o usuário terá a opção de criar uma impressora localmente.</span><span class="sxs-lookup"><span data-stu-id="c2267-105">If the user selects a printer, the function attempts to create a connection to it; if a suitable driver is not installed on the server, the user is given the option of creating a printer locally.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2267-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2267-106">Syntax</span></span>


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="c2267-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2267-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2267-108">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2267-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2267-109">Especifica a janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c2267-109">Specifies the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="c2267-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c2267-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2267-111">Esse parâmetro é reservado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2267-111">This parameter is reserved and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2267-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2267-112">Return value</span></span>

<span data-ttu-id="c2267-113">Se a função for bem sucedido e o usuário selecionar uma impressora, o valor de retorno será um identificador para a impressora selecionada.</span><span class="sxs-lookup"><span data-stu-id="c2267-113">If the function succeeds and the user selects a printer, the return value is a handle to the selected printer.</span></span>

<span data-ttu-id="c2267-114">Se a função falhar ou o usuário cancelar a caixa de diálogo sem selecionar uma impressora, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c2267-114">If the function fails, or the user cancels the dialog box without selecting a printer, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2267-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2267-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2267-116">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c2267-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c2267-117">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2267-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c2267-118">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="c2267-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c2267-119">A função **ConnectToPrinterDlg** tenta criar uma conexão com a impressora selecionada.</span><span class="sxs-lookup"><span data-stu-id="c2267-119">The **ConnectToPrinterDlg** function attempts to create a connection to the selected printer.</span></span> <span data-ttu-id="c2267-120">No entanto, se o servidor no qual a impressora reside não tiver um driver adequado instalado, a função oferece ao usuário a opção de criar uma impressora localmente.</span><span class="sxs-lookup"><span data-stu-id="c2267-120">However, if the server on which the printer resides does not have a suitable driver installed, the function offers the user the option of creating a printer locally.</span></span> <span data-ttu-id="c2267-121">Um aplicativo de chamada pode determinar se a função criou uma impressora localmente chamando [**Getprinter**](getprinter.md) com uma estrutura [**de \_ informações \_ da impressora 2**](printer-info-2.md) e, em seguida, examinando o membro **Attributes** da estrutura.</span><span class="sxs-lookup"><span data-stu-id="c2267-121">A calling application can determine whether the function has created a printer locally by calling [**GetPrinter**](getprinter.md) with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, then examining that structure's **Attributes** member.</span></span>

<span data-ttu-id="c2267-122">Um aplicativo deve chamar [**DeletePrinter**](deleteprinter.md) para excluir uma impressora local.</span><span class="sxs-lookup"><span data-stu-id="c2267-122">An application should call [**DeletePrinter**](deleteprinter.md) to delete a local printer.</span></span> <span data-ttu-id="c2267-123">Um aplicativo deve chamar [**DeletePrinterConnection**](deleteprinterconnection.md) para excluir uma conexão com uma impressora.</span><span class="sxs-lookup"><span data-stu-id="c2267-123">An application should call [**DeletePrinterConnection**](deleteprinterconnection.md) to delete a connection to a printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2267-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2267-124">Requirements</span></span>



| <span data-ttu-id="c2267-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2267-125">Requirement</span></span> | <span data-ttu-id="c2267-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c2267-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2267-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2267-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c2267-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2267-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c2267-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2267-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c2267-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2267-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2267-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2267-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2267-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2267-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c2267-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2267-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2267-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2267-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c2267-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c2267-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2267-136"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c2267-136"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="c2267-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2267-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2267-138">Impressão</span><span class="sxs-lookup"><span data-stu-id="c2267-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c2267-139">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="c2267-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c2267-140">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="c2267-140">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="c2267-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="c2267-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="c2267-142">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="c2267-142">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="c2267-143">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="c2267-143">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="c2267-144">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="c2267-144">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="c2267-145">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c2267-145">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




