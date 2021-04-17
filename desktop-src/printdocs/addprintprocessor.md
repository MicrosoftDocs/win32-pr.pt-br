---
description: A função AddPrintProcessor instala um processador de impressão no servidor especificado e adiciona o nome do processador de impressão à lista de processadores de impressão com suporte.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Função AddPrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770053"
---
# <a name="addprintprocessor-function"></a><span data-ttu-id="8a4f8-103">Função AddPrintProcessor</span><span class="sxs-lookup"><span data-stu-id="8a4f8-103">AddPrintProcessor function</span></span>

<span data-ttu-id="8a4f8-104">A função **AddPrintProcessor** instala um processador de impressão no servidor especificado e adiciona o nome do processador de impressão à lista de processadores de impressão com suporte.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-104">The **AddPrintProcessor** function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a4f8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a4f8-105">Syntax</span></span>


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="8a4f8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a4f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a4f8-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a4f8-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4f8-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o processador de impressão deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor should be installed.</span></span> <span data-ttu-id="8a4f8-109">Se esse parâmetro for **nulo**, o processador de impressão será instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-109">If this parameter is **NULL**, the print processor is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="8a4f8-110">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a4f8-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4f8-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="8a4f8-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="8a4f8-112">Se esse parâmetro for **NULL**, o ambiente atual do chamador/cliente (não do destino/servidor) será usado.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-112">If this parameter is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="8a4f8-113">*pPathName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a4f8-113">*pPathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4f8-114">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do arquivo que contém o processador de impressão.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-114">A pointer to a null-terminated string that specifies the name of the file that contains the print processor.</span></span> <span data-ttu-id="8a4f8-115">Esse arquivo deve estar no diretório de processador de impressão do sistema.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-115">This file must be in the system print-processor directory.</span></span>

</dd> <dt>

<span data-ttu-id="8a4f8-116">*pPrintProcessorName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a4f8-116">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a4f8-117">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-117">A pointer to a null-terminated string that specifies the name of the print processor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a4f8-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a4f8-118">Return value</span></span>

<span data-ttu-id="8a4f8-119">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8a4f8-120">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a4f8-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a4f8-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8a4f8-122">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8a4f8-123">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8a4f8-124">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8a4f8-125">O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="8a4f8-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="8a4f8-126">Antes de chamar a função **AddPrintProcessor** , um aplicativo deve verificar se o arquivo que contém o processador de impressão está armazenado no diretório do processador de impressão do sistema.</span><span class="sxs-lookup"><span data-stu-id="8a4f8-126">Before calling the **AddPrintProcessor** function, an application should verify that the file containing the print processor is stored in the system print-processor directory.</span></span> <span data-ttu-id="8a4f8-127">Um aplicativo pode recuperar o nome do diretório do processador de impressão do sistema chamando a função [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="8a4f8-127">An application can retrieve the name of the system print-processor directory by calling the [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) function.</span></span>

<span data-ttu-id="8a4f8-128">Um aplicativo pode determinar o nome dos processadores de impressão existentes chamando a função [**EnumPrintProcessors**](enumprintprocessors.md) .</span><span class="sxs-lookup"><span data-stu-id="8a4f8-128">An application can determine the name of existing print processors by calling the [**EnumPrintProcessors**](enumprintprocessors.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a4f8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a4f8-129">Requirements</span></span>



| <span data-ttu-id="8a4f8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a4f8-130">Requirement</span></span> | <span data-ttu-id="8a4f8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8a4f8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4f8-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a4f8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8a4f8-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8a4f8-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8a4f8-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a4f8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8a4f8-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8a4f8-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8a4f8-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8a4f8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a4f8-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a4f8-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8a4f8-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a4f8-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a4f8-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a4f8-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8a4f8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8a4f8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a4f8-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8a4f8-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8a4f8-142">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8a4f8-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8a4f8-143">**AddPrintProcessorW** (Unicode) e **AddPrintProcessorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8a4f8-143">**AddPrintProcessorW** (Unicode) and **AddPrintProcessorA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="8a4f8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a4f8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a4f8-145">Impressão</span><span class="sxs-lookup"><span data-stu-id="8a4f8-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8a4f8-146">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="8a4f8-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8a4f8-147">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="8a4f8-147">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="8a4f8-148">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="8a4f8-148">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)
</dt> </dl>

 

