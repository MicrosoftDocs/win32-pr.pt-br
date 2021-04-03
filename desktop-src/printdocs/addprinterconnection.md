---
description: A função AddPrinterConnection adiciona uma conexão à impressora especificada para o usuário atual.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: Função AddPrinterConnection (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829112"
---
# <a name="addprinterconnection-function"></a><span data-ttu-id="056ef-103">Função AddPrinterConnection</span><span class="sxs-lookup"><span data-stu-id="056ef-103">AddPrinterConnection function</span></span>

<span data-ttu-id="056ef-104">A função **AddPrinterConnection** adiciona uma conexão à impressora especificada para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="056ef-104">The **AddPrinterConnection** function adds a connection to the specified printer for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="056ef-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="056ef-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="056ef-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="056ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="056ef-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="056ef-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="056ef-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome de uma impressora à qual o usuário atual deseja estabelecer uma conexão.</span><span class="sxs-lookup"><span data-stu-id="056ef-108">A pointer to a null-terminated string that specifies the name of a printer to which the current user wishes to establish a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="056ef-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="056ef-109">Return value</span></span>

<span data-ttu-id="056ef-110">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="056ef-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="056ef-111">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="056ef-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="056ef-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="056ef-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="056ef-113">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="056ef-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="056ef-114">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="056ef-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="056ef-115">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="056ef-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="056ef-116">Quando o Windows faz uma conexão com uma impressora, pode ser necessário copiar arquivos de driver de impressora para o servidor no qual a impressora está conectada.</span><span class="sxs-lookup"><span data-stu-id="056ef-116">When Windows makes a connection to a printer, it may need to copy printer driver files to the server to which the printer is attached.</span></span> <span data-ttu-id="056ef-117">Se o usuário não tiver permissão para copiar arquivos para o local apropriado, a função **AddPrinterConnection** falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o acesso ao erro \_ \_ negado.</span><span class="sxs-lookup"><span data-stu-id="056ef-117">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection** function fails, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="056ef-118">Uma conexão de impressora estabelecida chamando **AddPrinterConnection** será enumerada quando [**EnumPrinters**](enumprinters.md) for chamado com *dwType* definido como conexão de \_ enumeração de impressora \_ .</span><span class="sxs-lookup"><span data-stu-id="056ef-118">A printer connection established by calling **AddPrinterConnection** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

## <a name="requirements"></a><span data-ttu-id="056ef-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="056ef-119">Requirements</span></span>



| <span data-ttu-id="056ef-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="056ef-120">Requirement</span></span> | <span data-ttu-id="056ef-121">Valor</span><span class="sxs-lookup"><span data-stu-id="056ef-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="056ef-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="056ef-122">Minimum supported client</span></span><br/> | <span data-ttu-id="056ef-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="056ef-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="056ef-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="056ef-124">Minimum supported server</span></span><br/> | <span data-ttu-id="056ef-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="056ef-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="056ef-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="056ef-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="056ef-127"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="056ef-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="056ef-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="056ef-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="056ef-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="056ef-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="056ef-130">DLL</span><span class="sxs-lookup"><span data-stu-id="056ef-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="056ef-131"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="056ef-131"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="056ef-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="056ef-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="056ef-133">**AddPrinterConnectionW** (Unicode) e **AddPrinterConnectionA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="056ef-133">**AddPrinterConnectionW** (Unicode) and **AddPrinterConnectionA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="056ef-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="056ef-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="056ef-135">Impressão</span><span class="sxs-lookup"><span data-stu-id="056ef-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="056ef-136">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="056ef-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="056ef-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="056ef-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="056ef-138">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="056ef-138">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="056ef-139">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="056ef-139">**EnumPrinters**</span></span>](enumprinters.md)
</dt> </dl>

 

