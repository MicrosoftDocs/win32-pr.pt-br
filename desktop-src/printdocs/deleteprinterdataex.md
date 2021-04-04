---
description: A função DeletePrinterDataEx exclui um valor especificado dos dados de configuração para uma impressora.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: Função DeletePrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662451"
---
# <a name="deleteprinterdataex-function"></a><span data-ttu-id="36b0d-103">Função DeletePrinterDataEx</span><span class="sxs-lookup"><span data-stu-id="36b0d-103">DeletePrinterDataEx function</span></span>

<span data-ttu-id="36b0d-104">A função **DeletePrinterDataEx** exclui um valor especificado dos dados de configuração para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="36b0d-104">The **DeletePrinterDataEx** function deletes a specified value from the configuration data for a printer.</span></span> <span data-ttu-id="36b0d-105">Os dados de configuração de uma impressora consistem em um conjunto de valores nomeados e digitados armazenados em uma hierarquia de chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="36b0d-105">A printer's configuration data consists of a set of named and typed values stored in a hierarchy of registry keys.</span></span> <span data-ttu-id="36b0d-106">A função exclui um valor especificado em uma chave especificada.</span><span class="sxs-lookup"><span data-stu-id="36b0d-106">The function deletes a specified value under a specified key.</span></span>

<span data-ttu-id="36b0d-107">Assim como a função [**DeletePrinterData**](deleteprinterdata.md) , **DeletePrinterDataEx** pode excluir valores armazenados pela função [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="36b0d-107">Like the [**DeletePrinterData**](deleteprinterdata.md) function, **DeletePrinterDataEx** can delete values stored by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="36b0d-108">Além disso, o **DeletePrinterDataEx** pode excluir valores armazenados em uma chave especificada pela função [**SetPrinterDataEx**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="36b0d-108">In addition, **DeletePrinterDataEx** can delete values stored under a specified key by the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="36b0d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36b0d-109">Syntax</span></span>


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="36b0d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36b0d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36b0d-111">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36b0d-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36b0d-112">Um identificador para a impressora para a qual a função exclui um valor.</span><span class="sxs-lookup"><span data-stu-id="36b0d-112">A handle to the printer for which the function deletes a value.</span></span> <span data-ttu-id="36b0d-113">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="36b0d-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="36b0d-114">*pKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36b0d-114">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36b0d-115">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém o valor a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="36b0d-115">A pointer to a null-terminated string that specifies the key containing the value to delete.</span></span> <span data-ttu-id="36b0d-116">Use o caractere de barra invertida ( \\ ) como um delimitador para especificar um caminho que tenha uma ou mais subchaves.</span><span class="sxs-lookup"><span data-stu-id="36b0d-116">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="36b0d-117">Se *pKeyName* for **nulo** ou uma cadeia de caracteres vazia, **DeletePrinterDataEx** retornará um \_ parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="36b0d-117">If *pKeyName* is **NULL** or an empty string, **DeletePrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="36b0d-118">*valores principais* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="36b0d-118">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36b0d-119">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do valor a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="36b0d-119">A pointer to a null-terminated string that specifies the name of the value to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36b0d-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36b0d-120">Return value</span></span>

<span data-ttu-id="36b0d-121">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="36b0d-121">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="36b0d-122">Se a função falhar, o valor de retorno será um código de erro do sistema.</span><span class="sxs-lookup"><span data-stu-id="36b0d-122">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="36b0d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="36b0d-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="36b0d-124">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="36b0d-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="36b0d-125">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36b0d-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="36b0d-126">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="36b0d-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="36b0d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36b0d-127">Requirements</span></span>



| <span data-ttu-id="36b0d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="36b0d-128">Requirement</span></span> | <span data-ttu-id="36b0d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="36b0d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36b0d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36b0d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="36b0d-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="36b0d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36b0d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36b0d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="36b0d-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="36b0d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="36b0d-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="36b0d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="36b0d-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36b0d-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="36b0d-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36b0d-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="36b0d-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36b0d-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="36b0d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="36b0d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36b0d-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="36b0d-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="36b0d-140">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="36b0d-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="36b0d-141">**DeletePrinterDataExW** (Unicode) e **DeletePrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="36b0d-141">**DeletePrinterDataExW** (Unicode) and **DeletePrinterDataExA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="36b0d-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="36b0d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36b0d-143">Impressão</span><span class="sxs-lookup"><span data-stu-id="36b0d-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="36b0d-144">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="36b0d-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="36b0d-145">**DeletePrinterKey**</span><span class="sxs-lookup"><span data-stu-id="36b0d-145">**DeletePrinterKey**</span></span>](deleteprinterkey.md)
</dt> <dt>

[<span data-ttu-id="36b0d-146">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="36b0d-146">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="36b0d-147">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="36b0d-147">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="36b0d-148">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="36b0d-148">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="36b0d-149">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="36b0d-149">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="36b0d-150">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="36b0d-150">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




