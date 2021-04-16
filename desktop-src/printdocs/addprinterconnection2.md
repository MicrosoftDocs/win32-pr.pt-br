---
description: Adiciona uma conexão à impressora especificada para o usuário atual e especifica os detalhes da conexão.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: Função AddPrinterConnection2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782213"
---
# <a name="addprinterconnection2-function"></a><span data-ttu-id="d5a6f-103">Função AddPrinterConnection2</span><span class="sxs-lookup"><span data-stu-id="d5a6f-103">AddPrinterConnection2 function</span></span>

<span data-ttu-id="d5a6f-104">Adiciona uma conexão à impressora especificada para o usuário atual e especifica os detalhes da conexão.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-104">Adds a connection to the specified printer for the current user and specifies connection details.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5a6f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5a6f-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d5a6f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5a6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a6f-107">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5a6f-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5a6f-108">Um identificador para a janela pai no qual a caixa de diálogo será exibida se o sistema de impressão precisar baixar um driver de impressora do servidor de impressão para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-108">A handle to the parent window in which the dialog box will be displayed if the print system must download a printer driver from the print server for this connection.</span></span>

</dd> <dt>

<span data-ttu-id="d5a6f-109">*pszName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5a6f-109">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5a6f-110">Um ponteiro para uma cadeia de caracteres de constante terminada em nulo especificando o nome da impressora à qual o usuário atual deseja se conectar.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-110">A pointer to a constant null-terminated string specifying the name of the printer to which the current user wishes to connect.</span></span>

</dd> <dt>

<span data-ttu-id="d5a6f-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="d5a6f-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="d5a6f-112">A versão da estrutura apontada por *pConnectionInfo*.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-112">The version of the structure pointed to by *pConnectionInfo*.</span></span> <span data-ttu-id="d5a6f-113">Atualmente, somente o nível 1 é definido, portanto, o valor de *dwLevel* deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-113">Currently, only level 1 is defined so the value of *dwLevel* must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="d5a6f-114">*pConnectionInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d5a6f-114">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5a6f-115">Um ponteiro para uma estrutura de [**informações de conexão de impressora \_ \_ \_ 1**](printer-connection-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="d5a6f-115">A pointer to a [**PRINTER\_CONNECTION\_INFO\_1**](printer-connection-info-1.md) structure.</span></span> <span data-ttu-id="d5a6f-116">Consulte a seção comentários para obter mais informações sobre esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-116">See the Remarks section for more about this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5a6f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5a6f-117">Return value</span></span>

<span data-ttu-id="d5a6f-118">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d5a6f-119">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="d5a6f-120">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="d5a6f-120">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5a6f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5a6f-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5a6f-122">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d5a6f-123">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d5a6f-124">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d5a6f-125">Quando o Windows Vista faz uma conexão com uma impressora, pode ser necessário copiar arquivos de driver de impressora do servidor ao qual a impressora está conectada.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-125">When Windows Vista makes a connection to a printer, it may need to copy printer driver files from the server to which the printer is attached.</span></span> <span data-ttu-id="d5a6f-126">Se o usuário não tiver permissão para copiar arquivos para o local apropriado, a função **AddPrinterConnection2** falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o \_ acesso ao erro \_ negado.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-126">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection2** function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="d5a6f-127">Se os arquivos de driver de impressora precisarem ser copiados do servidor de impressão, mas não puderem ser copiados silenciosamente devido às políticas de grupo que estão em vigor e \_ \_ a conexão de impressora sem \_ interface do usuário estiver definida em *pConnectionInfo->dwFlags*, nenhuma caixa de diálogo será exibida e a chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-127">If the printer driver files must be copied from the print server but cannot be copied silently due to the group policies that are in effect and PRINTER\_CONNECTION\_NO\_UI is set in *pConnectionInfo->dwFlags*, no dialog boxes will be displayed and the call will fail.</span></span>

<span data-ttu-id="d5a6f-128">Se o driver de impressora local pode ser usado para renderizar trabalhos de impressão para esta impressora e a versão do driver local não deve corresponder à versão do driver de impressora no servidor, defina \_ incompatibilidade de conexão de impressora \_ em *PConnectionInfo->dwFlags* e atribua o ponteiro a uma variável de cadeia de caracteres que contenha o caminho para o driver de impressora local para *pConnectionInfo->pszDriverName*.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-128">If the local printer driver can be used to render print jobs for this printer and the version of the local driver must not match the version of the printer driver on the server, set PRINTER\_CONNECTION\_MISMATCH in *pConnectionInfo->dwFlags* and assign the pointer to a string variable that contains the path to the local printer driver to *pConnectionInfo->pszDriverName*.</span></span>

<span data-ttu-id="d5a6f-129">Uma conexão de impressora estabelecida pela chamada de **AddPrinterConnection2** será enumerada quando [**EnumPrinters**](enumprinters.md) for chamado com *dwType* definido como conexão de \_ enumeração de impressora \_ .</span><span class="sxs-lookup"><span data-stu-id="d5a6f-129">A printer connection that is established by calling **AddPrinterConnection2** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

<span data-ttu-id="d5a6f-130">Não há suporte para a versão ANSI dessa função, **AddPrinterConnection2A**, e **\_ não \_ há suporte para** retorno de erro.</span><span class="sxs-lookup"><span data-stu-id="d5a6f-130">The ANSI version of this function, **AddPrinterConnection2A**, is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a6f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5a6f-131">Requirements</span></span>



| <span data-ttu-id="d5a6f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5a6f-132">Requirement</span></span> | <span data-ttu-id="d5a6f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d5a6f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a6f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5a6f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a6f-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5a6f-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d5a6f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5a6f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a6f-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5a6f-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d5a6f-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5a6f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5a6f-139"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5a6f-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d5a6f-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5a6f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5a6f-141"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5a6f-141"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d5a6f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d5a6f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5a6f-143"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d5a6f-143"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d5a6f-144">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d5a6f-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5a6f-145">**AddPrinterConnection2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="d5a6f-145">**AddPrinterConnection2W** (Unicode)</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="d5a6f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5a6f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5a6f-147">Impressão</span><span class="sxs-lookup"><span data-stu-id="d5a6f-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d5a6f-148">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="d5a6f-148">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d5a6f-149">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="d5a6f-149">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="d5a6f-150">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="d5a6f-150">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="d5a6f-151">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="d5a6f-151">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> </dl>

 

