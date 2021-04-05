---
description: A função EnumPrinterDataEx enumera todos os nomes de valor e dados para uma impressora e chave especificadas.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: Função EnumPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662606"
---
# <a name="enumprinterdataex-function"></a><span data-ttu-id="0e19b-103">Função EnumPrinterDataEx</span><span class="sxs-lookup"><span data-stu-id="0e19b-103">EnumPrinterDataEx function</span></span>

<span data-ttu-id="0e19b-104">A função **EnumPrinterDataEx** enumera todos os nomes de valor e dados para uma impressora e chave especificadas.</span><span class="sxs-lookup"><span data-stu-id="0e19b-104">The **EnumPrinterDataEx** function enumerates all value names and data for a specified printer and key.</span></span>

<span data-ttu-id="0e19b-105">Os dados da impressora são armazenados no registro.</span><span class="sxs-lookup"><span data-stu-id="0e19b-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="0e19b-106">Ao enumerar os dados da impressora, não chame funções de registro que possam alterar os dados.</span><span class="sxs-lookup"><span data-stu-id="0e19b-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e19b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e19b-107">Syntax</span></span>


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a><span data-ttu-id="0e19b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e19b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e19b-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e19b-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e19b-110">Um identificador para a impressora para a qual a função recupera dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="0e19b-110">A handle to the printer for which the function retrieves configuration data.</span></span> <span data-ttu-id="0e19b-111">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="0e19b-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="0e19b-112">*pKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e19b-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e19b-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém os valores a serem enumerados.</span><span class="sxs-lookup"><span data-stu-id="0e19b-113">A pointer to a null-terminated string that specifies the key containing the values to enumerate.</span></span> <span data-ttu-id="0e19b-114">Use o caractere de barra invertida ( \\ ) como um delimitador para especificar um caminho com uma ou mais subchaves.</span><span class="sxs-lookup"><span data-stu-id="0e19b-114">Use the backslash ( \\ ) character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="0e19b-115">**EnumPrinterDataEx** enumera todos os valores da chave, mas não enumera os valores de subchaves da chave especificada.</span><span class="sxs-lookup"><span data-stu-id="0e19b-115">**EnumPrinterDataEx** enumerates all values of the key, but does not enumerate values of subkeys of the specified key.</span></span> <span data-ttu-id="0e19b-116">Use a função [**EnumPrinterKey**](enumprinterkey.md) para enumerar subchaves.</span><span class="sxs-lookup"><span data-stu-id="0e19b-116">Use the [**EnumPrinterKey**](enumprinterkey.md) function to enumerate subkeys.</span></span>

<span data-ttu-id="0e19b-117">Se *pKeyName* for **nulo** ou uma cadeia de caracteres vazia, **EnumPrinterDataEx** retornará um \_ parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="0e19b-117">If *pKeyName* is **NULL** or an empty string, **EnumPrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="0e19b-118">*pEnumValues* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0e19b-118">*pEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e19b-119">Um ponteiro para um buffer que recebe uma matriz de estruturas de [**\_ \_ valores de enumeração de impressora**](printer-enum-values.md) .</span><span class="sxs-lookup"><span data-stu-id="0e19b-119">A pointer to a buffer that receives an array of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures.</span></span> <span data-ttu-id="0e19b-120">Cada estrutura contém o nome do valor, o tipo, os dados e os tamanhos de um valor sob a chave.</span><span class="sxs-lookup"><span data-stu-id="0e19b-120">Each structure contains the value name, type, data, and sizes of a value under the key.</span></span>

</dd> <dt>

<span data-ttu-id="0e19b-121">*cbEnumValues* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0e19b-121">*cbEnumValues* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e19b-122">O tamanho, em bytes, do buffer apontado por *pcbEnumValues*.</span><span class="sxs-lookup"><span data-stu-id="0e19b-122">The size, in bytes, of the buffer pointed to by *pcbEnumValues*.</span></span> <span data-ttu-id="0e19b-123">Se você definir *cbEnumValues* como zero, o parâmetro *pcbEnumValues* retornará o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="0e19b-123">If you set *cbEnumValues* to zero, the *pcbEnumValues* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="0e19b-124">*pcbEnumValues* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0e19b-124">*pcbEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e19b-125">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de configuração recuperados.</span><span class="sxs-lookup"><span data-stu-id="0e19b-125">A pointer to a variable that receives the size, in bytes, of the retrieved configuration data.</span></span> <span data-ttu-id="0e19b-126">Se o tamanho do buffer especificado por *cbEnumValues* for muito pequeno, a função retornará um erro com \_ mais \_ dados e *pcbEnumValues* indicará o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="0e19b-126">If the buffer size specified by *cbEnumValues* is too small, the function returns ERROR\_MORE\_DATA and *pcbEnumValues* indicates the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="0e19b-127">*pnEnumValues* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0e19b-127">*pnEnumValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e19b-128">Um ponteiro para uma variável que recebe o número de estruturas de [**\_ \_ valores de enumeração de impressora**](printer-enum-values.md) retornado em *pEnumValues*.</span><span class="sxs-lookup"><span data-stu-id="0e19b-128">A pointer to a variable that receives the number of [**PRINTER\_ENUM\_VALUES**](printer-enum-values.md) structures returned in *pEnumValues*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e19b-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e19b-129">Return value</span></span>

<span data-ttu-id="0e19b-130">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="0e19b-130">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0e19b-131">Se a função falhar, o valor de retorno será um código de erro do sistema.</span><span class="sxs-lookup"><span data-stu-id="0e19b-131">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e19b-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e19b-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0e19b-133">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0e19b-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0e19b-134">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e19b-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0e19b-135">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="0e19b-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="0e19b-136">**EnumPrinterDataEx** recupera os dados de configuração de impressora definidos pelas funções [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="0e19b-136">**EnumPrinterDataEx** retrieves printer configuration data set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e19b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e19b-137">Requirements</span></span>



| <span data-ttu-id="0e19b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e19b-138">Requirement</span></span> | <span data-ttu-id="0e19b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="0e19b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e19b-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e19b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="0e19b-141">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e19b-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0e19b-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e19b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="0e19b-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0e19b-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0e19b-144">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0e19b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e19b-145"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e19b-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0e19b-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0e19b-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e19b-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e19b-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0e19b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0e19b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e19b-149"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0e19b-149"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0e19b-150">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0e19b-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e19b-151">**EnumPrinterDataExW** (Unicode) e **EnumPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0e19b-151">**EnumPrinterDataExW** (Unicode) and **EnumPrinterDataExA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="0e19b-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e19b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e19b-153">Impressão</span><span class="sxs-lookup"><span data-stu-id="0e19b-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0e19b-154">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="0e19b-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0e19b-155">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="0e19b-155">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="0e19b-156">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="0e19b-156">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="0e19b-157">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="0e19b-157">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="0e19b-158">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="0e19b-158">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="0e19b-159">**\_valores de enumeração da impressora \_**</span><span class="sxs-lookup"><span data-stu-id="0e19b-159">**PRINTER\_ENUM\_VALUES**</span></span>](printer-enum-values.md)
</dt> <dt>

[<span data-ttu-id="0e19b-160">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="0e19b-160">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="0e19b-161">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="0e19b-161">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




