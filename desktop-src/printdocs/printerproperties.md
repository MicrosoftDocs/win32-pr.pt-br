---
description: A função Impressorasproperties exibe uma folha de propriedades da impressora para a impressora especificada.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: Função printerproperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: e7e2c8586c06b2cb64a0e499bd05a6b6016de0a6
ms.sourcegitcommit: c77ed4d933c9f30af0ca0e095a75ad2bdd4d8bf8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/31/2021
ms.locfileid: "106011182"
---
# <a name="printerproperties-function"></a><span data-ttu-id="d7928-103">Função printerproperties</span><span class="sxs-lookup"><span data-stu-id="d7928-103">PrinterProperties function</span></span>

<span data-ttu-id="d7928-104">A função **impressorasproperties** exibe uma folha de propriedades da impressora para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="d7928-104">The **PrinterProperties** function displays a printer-properties property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7928-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7928-105">Syntax</span></span>


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="d7928-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7928-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7928-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7928-108">Um identificador para a janela pai da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="d7928-108">A handle to the parent window of the property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="d7928-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d7928-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7928-110">Um identificador para um objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="d7928-110">A handle to a printer object.</span></span> <span data-ttu-id="d7928-111">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="d7928-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7928-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7928-112">Return value</span></span>

<span data-ttu-id="d7928-113">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d7928-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d7928-114">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="d7928-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7928-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7928-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d7928-116">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d7928-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d7928-117">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d7928-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d7928-118">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="d7928-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7928-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7928-119">Requirements</span></span>



| <span data-ttu-id="d7928-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7928-120">Requirement</span></span> | <span data-ttu-id="d7928-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d7928-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7928-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7928-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7928-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7928-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7928-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7928-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7928-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7928-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7928-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d7928-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7928-127"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7928-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d7928-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7928-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7928-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7928-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d7928-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d7928-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7928-131"><dt>winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d7928-131"><dt>winspool.drv</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d7928-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7928-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7928-133">Impressão</span><span class="sxs-lookup"><span data-stu-id="d7928-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d7928-134">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="d7928-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d7928-135">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="d7928-135">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="d7928-136">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d7928-136">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




