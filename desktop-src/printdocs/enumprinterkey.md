---
description: A função EnumPrinterKey enumera as subchaves de uma chave especificada para uma impressora especificada.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: Função EnumPrinterKey (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d9af6a9ef26612385cee68eba9733c148cd36b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297148"
---
# <a name="enumprinterkey-function"></a><span data-ttu-id="1ecb1-103">Função EnumPrinterKey</span><span class="sxs-lookup"><span data-stu-id="1ecb1-103">EnumPrinterKey function</span></span>

<span data-ttu-id="1ecb1-104">A função **EnumPrinterKey** enumera as subchaves de uma chave especificada para uma impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-104">The **EnumPrinterKey** function enumerates the subkeys of a specified key for a specified printer.</span></span>

<span data-ttu-id="1ecb1-105">Os dados da impressora são armazenados no registro.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-105">Printer data is stored in the registry.</span></span> <span data-ttu-id="1ecb1-106">Ao enumerar os dados da impressora, não chame funções de registro que possam alterar os dados.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-106">While enumerating printer data, do not call registry functions that might change the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ecb1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ecb1-107">Syntax</span></span>


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a><span data-ttu-id="1ecb1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ecb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ecb1-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ecb1-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ecb1-110">Um identificador para a impressora para a qual a função enumera subchaves.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-110">A handle to the printer for which the function enumerates subkeys.</span></span> <span data-ttu-id="1ecb1-111">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="1ecb1-112">*pKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ecb1-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ecb1-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém as subchaves a serem enumeradas.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-113">A pointer to a null-terminated string that specifies the key containing the subkeys to enumerate.</span></span> <span data-ttu-id="1ecb1-114">Use o caractere de barra invertida ' \\ ' como um delimitador para especificar um caminho com uma ou mais subchaves.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-114">Use the backslash '\\' character as a delimiter to specify a path with one or more subkeys.</span></span> <span data-ttu-id="1ecb1-115">**EnumPrinterKey** enumera todas as subchaves da chave, mas não enumera as subchaves dessas subchaves.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-115">**EnumPrinterKey** enumerates all subkeys of the key, but does not enumerate the subkeys of those subkeys.</span></span>

<span data-ttu-id="1ecb1-116">Se *pKeyName* for uma cadeia de caracteres vazia (""), **EnumPrinterKey** enumerará a chave de nível superior para a impressora.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-116">If *pKeyName* is an empty string (""), **EnumPrinterKey** enumerates the top-level key for the printer.</span></span> <span data-ttu-id="1ecb1-117">Se *pKeyName* for **nulo**, **EnumPrinterKey** retornará um \_ parâmetro inválido de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="1ecb1-117">If *pKeyName* is **NULL**, **EnumPrinterKey** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="1ecb1-118">*pSubkey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ecb1-118">*pSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ecb1-119">Um ponteiro para um buffer que recebe uma matriz de nomes de subchaves terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-119">A pointer to a buffer that receives an array of null-terminated subkey names.</span></span> <span data-ttu-id="1ecb1-120">A matriz é terminada por dois caracteres nulos.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-120">The array is terminated by two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="1ecb1-121">*cbSubkey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ecb1-121">*cbSubkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ecb1-122">O tamanho, em bytes, do buffer apontado por *pSubkey*.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-122">The size, in bytes, of the buffer pointed to by *pSubkey*.</span></span> <span data-ttu-id="1ecb1-123">Se você definir *cbSubkey* como zero, o parâmetro *pcbSubkey* retornará o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-123">If you set *cbSubkey* to zero, the *pcbSubkey* parameter returns the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="1ecb1-124">*pcbSubkey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ecb1-124">*pcbSubkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ecb1-125">Um ponteiro para uma variável que recebe o número de bytes recuperados no buffer *pSubkey* .</span><span class="sxs-lookup"><span data-stu-id="1ecb1-125">A pointer to a variable that receives the number of bytes retrieved in the *pSubkey* buffer.</span></span> <span data-ttu-id="1ecb1-126">Se o tamanho do buffer especificado por *cbSubkey* for muito pequeno, a função retornará um erro com \_ mais \_ dados e *pcbSubkey* indicará o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-126">If the buffer size specified by *cbSubkey* is too small, the function returns ERROR\_MORE\_DATA and *pcbSubkey* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ecb1-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ecb1-127">Return value</span></span>

<span data-ttu-id="1ecb1-128">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-128">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="1ecb1-129">Se a função falhar, o valor de retorno será um código de erro do sistema.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-129">If the function fails, the return value is a system error code.</span></span> <span data-ttu-id="1ecb1-130">Se *pKeyName* não existir, o valor de retorno será o \_ arquivo de erro \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-130">If *pKeyName* does not exist, the return value is ERROR\_FILE\_NOT\_FOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ecb1-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ecb1-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1ecb1-132">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1ecb1-133">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1ecb1-134">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1ecb1-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ecb1-135">Requirements</span></span>



| <span data-ttu-id="1ecb1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ecb1-136">Requirement</span></span> | <span data-ttu-id="1ecb1-137">Valor</span><span class="sxs-lookup"><span data-stu-id="1ecb1-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecb1-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ecb1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1ecb1-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ecb1-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1ecb1-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ecb1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1ecb1-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ecb1-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1ecb1-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ecb1-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ecb1-143"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb1-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1ecb1-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ecb1-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ecb1-145"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb1-145"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1ecb1-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1ecb1-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ecb1-147"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb1-147"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1ecb1-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1ecb1-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1ecb1-149">**EnumPrinterKeyW** (Unicode) e **EnumPrinterKeyA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1ecb1-149">**EnumPrinterKeyW** (Unicode) and **EnumPrinterKeyA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="1ecb1-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ecb1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ecb1-151">Impressão</span><span class="sxs-lookup"><span data-stu-id="1ecb1-151">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1ecb1-152">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="1ecb1-152">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1ecb1-153">**DeletePrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="1ecb1-153">**DeletePrinterDataEx**</span></span>](deleteprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="1ecb1-154">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="1ecb1-154">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="1ecb1-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="1ecb1-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="1ecb1-156">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="1ecb1-156">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




