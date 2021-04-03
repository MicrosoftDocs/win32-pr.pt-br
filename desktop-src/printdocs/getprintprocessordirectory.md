---
description: A função GetPrintProcessorDirectory recupera o caminho para o diretório do processador de impressão no servidor especificado.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: Função GetPrintProcessorDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837148"
---
# <a name="getprintprocessordirectory-function"></a><span data-ttu-id="a4853-103">Função GetPrintProcessorDirectory</span><span class="sxs-lookup"><span data-stu-id="a4853-103">GetPrintProcessorDirectory function</span></span>

<span data-ttu-id="a4853-104">A função **GetPrintProcessorDirectory** recupera o caminho para o diretório do processador de impressão no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="a4853-104">The **GetPrintProcessorDirectory** function retrieves the path to the print processor directory on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4853-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4853-105">Syntax</span></span>


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="a4853-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4853-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4853-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4853-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4853-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a4853-108">A pointer to a null-terminated string that specifies the name of the server.</span></span> <span data-ttu-id="a4853-109">Se esse parâmetro for **NULL**, um caminho local será retornado.</span><span class="sxs-lookup"><span data-stu-id="a4853-109">If this parameter is **NULL**, a local path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="a4853-110">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4853-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4853-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a4853-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="a4853-112">Se esse parâmetro for **NULL**, o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.</span><span class="sxs-lookup"><span data-stu-id="a4853-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="a4853-113">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a4853-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4853-114">O nível da estrutura.</span><span class="sxs-lookup"><span data-stu-id="a4853-114">The structure level.</span></span> <span data-ttu-id="a4853-115">Esse valor deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="a4853-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="a4853-116">*pPrintProcessorInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4853-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4853-117">Um ponteiro para um buffer que recebe o caminho.</span><span class="sxs-lookup"><span data-stu-id="a4853-117">A pointer to a buffer that receives the path.</span></span> <span data-ttu-id="a4853-118">Observe que, para sistemas operacionais anteriores ao Windows Server 2003 SP 1, o caminho está no formato local para o servidor, não no verdadeiro formato remoto.</span><span class="sxs-lookup"><span data-stu-id="a4853-118">Note that, for operating systems prior to Windows Server 2003 SP 1, the path is in the local format for the server, not the true remote format.</span></span> <span data-ttu-id="a4853-119">Por exemplo, o caminho é fornecido como "% windir% \\ System32 \\ spool \\ prtprocs \\ % Environment" em vez de " \\ \\ ServerName \\ Print $ \\ prtprocs \\ % Environment%", mesmo quando chamado para um servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="a4853-119">For example, the path is given as "%Windir%\\System32\\Spool\\Prtprocs\\%Environment%" instead of "\\\\ServerName\\Print$\\Prtprocs\\%Environment%", even when called for a remote server.</span></span> <span data-ttu-id="a4853-120">Para os sistemas operacionais Windows Server 2003 SP 1 e posterior, o caminho remoto verdadeiro é retornado.</span><span class="sxs-lookup"><span data-stu-id="a4853-120">For the operating systems Windows Server 2003 SP 1 and later, the true remote path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="a4853-121">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a4853-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4853-122">O tamanho do buffer apontado por *pPrintProcessorInfo*.</span><span class="sxs-lookup"><span data-stu-id="a4853-122">The size of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="a4853-123">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4853-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4853-124">Um ponteiro para um valor que especifica o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="a4853-124">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4853-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4853-125">Return value</span></span>

<span data-ttu-id="a4853-126">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a4853-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a4853-127">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="a4853-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4853-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4853-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a4853-129">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a4853-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a4853-130">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4853-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a4853-131">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="a4853-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a4853-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4853-132">Requirements</span></span>



| <span data-ttu-id="a4853-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4853-133">Requirement</span></span> | <span data-ttu-id="a4853-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a4853-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4853-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4853-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a4853-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4853-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a4853-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4853-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a4853-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4853-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a4853-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a4853-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4853-140"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4853-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a4853-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4853-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4853-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4853-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a4853-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a4853-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4853-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a4853-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a4853-145">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a4853-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a4853-146">**GetPrintProcessorDirectoryW** (Unicode) e **GetPrintProcessorDirectoryA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a4853-146">**GetPrintProcessorDirectoryW** (Unicode) and **GetPrintProcessorDirectoryA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a4853-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4853-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4853-148">Impressão</span><span class="sxs-lookup"><span data-stu-id="a4853-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a4853-149">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="a4853-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a4853-150">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="a4853-150">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

 




