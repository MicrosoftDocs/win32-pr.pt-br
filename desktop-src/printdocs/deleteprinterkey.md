---
description: A função DeletePrinterKey exclui uma chave especificada e todas as suas subchaves para uma impressora especificada.
ms.assetid: 0bd81b43-5c1e-4989-8350-2ec0dc215f28
title: Função DeletePrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterKey
- DeletePrinterKeyA
- DeletePrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 4be073f7832f647e156dbd3b5e12d23ffe6acc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662571"
---
# <a name="deleteprinterkey-function"></a><span data-ttu-id="3333e-103">Função DeletePrinterKey</span><span class="sxs-lookup"><span data-stu-id="3333e-103">DeletePrinterKey function</span></span>

<span data-ttu-id="3333e-104">A função **DeletePrinterKey** exclui uma chave especificada e todas as suas subchaves para uma impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="3333e-104">The **DeletePrinterKey** function deletes a specified key and all its subkeys for a specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3333e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3333e-105">Syntax</span></span>


```C++
DWORD DeletePrinterKey(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName
);
```



## <a name="parameters"></a><span data-ttu-id="3333e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3333e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3333e-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3333e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3333e-108">Um identificador para a impressora para a qual a função exclui uma chave.</span><span class="sxs-lookup"><span data-stu-id="3333e-108">A handle to the printer for which the function deletes a key.</span></span> <span data-ttu-id="3333e-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="3333e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="3333e-110">*pKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3333e-110">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3333e-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="3333e-111">A pointer to a null-terminated string that specifies the key to delete.</span></span> <span data-ttu-id="3333e-112">Use o caractere de barra invertida ( \\ ) como um delimitador para especificar um caminho com uma ou mais subchaves.</span><span class="sxs-lookup"><span data-stu-id="3333e-112">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span>

<span data-ttu-id="3333e-113">Se *pKeyName* for uma cadeia de caracteres vazia (""), **DeletePrinterKey** excluirá todas as chaves abaixo da chave de nível superior da impressora.</span><span class="sxs-lookup"><span data-stu-id="3333e-113">If *pKeyName* is an empty string (""), **DeletePrinterKey** deletes all keys below the top-level key for the printer.</span></span> <span data-ttu-id="3333e-114">Se *pKeyName* for **nulo**, **DeletePrinterKey** retornará um \_ parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="3333e-114">If *pKeyName* is **NULL**, **DeletePrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3333e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3333e-115">Return value</span></span>

<span data-ttu-id="3333e-116">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="3333e-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3333e-117">Se a função falhar, o valor de retorno será um código de erro do sistema.</span><span class="sxs-lookup"><span data-stu-id="3333e-117">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3333e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3333e-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3333e-119">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3333e-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3333e-120">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3333e-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3333e-121">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="3333e-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3333e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3333e-122">Requirements</span></span>



| <span data-ttu-id="3333e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3333e-123">Requirement</span></span> | <span data-ttu-id="3333e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3333e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3333e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3333e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3333e-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3333e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3333e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3333e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3333e-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3333e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3333e-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3333e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3333e-130"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3333e-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3333e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3333e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="3333e-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3333e-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3333e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3333e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3333e-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3333e-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3333e-135">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3333e-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3333e-136">**DeletePrinterKeyW** (Unicode) e **DeletePrinterKeyA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3333e-136">**DeletePrinterKeyW** (Unicode) and **DeletePrinterKeyA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="3333e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3333e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3333e-138">Impressão</span><span class="sxs-lookup"><span data-stu-id="3333e-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3333e-139">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="3333e-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3333e-140">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="3333e-140">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="3333e-141">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="3333e-141">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="3333e-142">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="3333e-142">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="3333e-143">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="3333e-143">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="3333e-144">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="3333e-144">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3333e-145">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="3333e-145">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




