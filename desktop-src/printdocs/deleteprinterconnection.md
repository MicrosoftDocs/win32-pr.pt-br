---
description: A função DeletePrinterConnection exclui uma conexão a uma impressora que foi estabelecida por uma chamada para AddPrinterConnection ou ConnectToPrinterDlg.
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: Função DeletePrinterConnection (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c524e3bcc79efc2207839b3d3a95051e2eb8bae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798538"
---
# <a name="deleteprinterconnection-function"></a><span data-ttu-id="88a93-103">Função DeletePrinterConnection</span><span class="sxs-lookup"><span data-stu-id="88a93-103">DeletePrinterConnection function</span></span>

<span data-ttu-id="88a93-104">A função **DeletePrinterConnection** exclui uma conexão a uma impressora que foi estabelecida por uma chamada para [**AddPrinterConnection**](addprinterconnection.md) ou [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span><span class="sxs-lookup"><span data-stu-id="88a93-104">The **DeletePrinterConnection** function deletes a connection to a printer that was established by a call to [**AddPrinterConnection**](addprinterconnection.md) or [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="88a93-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88a93-105">Syntax</span></span>


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="88a93-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88a93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a93-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="88a93-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88a93-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da conexão de impressora a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="88a93-108">Pointer to a null-terminated string that specifies the name of the printer connection to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a93-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88a93-109">Return value</span></span>

<span data-ttu-id="88a93-110">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="88a93-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="88a93-111">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="88a93-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="88a93-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="88a93-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="88a93-113">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="88a93-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="88a93-114">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="88a93-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="88a93-115">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="88a93-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="88a93-116">A função **DeletePrinterConnection** não exclui arquivos de driver de impressora que foram copiados para o servidor ao qual a impressora está conectada.</span><span class="sxs-lookup"><span data-stu-id="88a93-116">The **DeletePrinterConnection** function does not delete any printer driver files that were copied to the server to which the printer is attached.</span></span>

## <a name="requirements"></a><span data-ttu-id="88a93-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88a93-117">Requirements</span></span>



| <span data-ttu-id="88a93-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="88a93-118">Requirement</span></span> | <span data-ttu-id="88a93-119">Valor</span><span class="sxs-lookup"><span data-stu-id="88a93-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88a93-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88a93-120">Minimum supported client</span></span><br/> | <span data-ttu-id="88a93-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88a93-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="88a93-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88a93-122">Minimum supported server</span></span><br/> | <span data-ttu-id="88a93-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="88a93-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="88a93-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="88a93-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="88a93-125"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88a93-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="88a93-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="88a93-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="88a93-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88a93-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="88a93-128">DLL</span><span class="sxs-lookup"><span data-stu-id="88a93-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88a93-129"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="88a93-129"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="88a93-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="88a93-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="88a93-131">**DeletePrinterConnectionW** (Unicode) e **DeletePrinterConnectionA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="88a93-131">**DeletePrinterConnectionW** (Unicode) and **DeletePrinterConnectionA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="88a93-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="88a93-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88a93-133">Impressão</span><span class="sxs-lookup"><span data-stu-id="88a93-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="88a93-134">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="88a93-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="88a93-135">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="88a93-135">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="88a93-136">**AddPrinterConnection2**</span><span class="sxs-lookup"><span data-stu-id="88a93-136">**AddPrinterConnection2**</span></span>](addprinterconnection2.md)
</dt> <dt>

[<span data-ttu-id="88a93-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="88a93-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> </dl>

 

 




