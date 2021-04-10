---
description: A função EnumPrinterData enumera dados de configuração para uma impressora especificada.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Função EnumPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169343"
---
# <a name="enumprinterdata-function"></a><span data-ttu-id="233c5-103">Função EnumPrinterData</span><span class="sxs-lookup"><span data-stu-id="233c5-103">EnumPrinterData function</span></span>

<span data-ttu-id="233c5-104">A função **EnumPrinterData** enumera dados de configuração para uma impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="233c5-104">The **EnumPrinterData** function enumerates configuration data for a specified printer.</span></span>

<span data-ttu-id="233c5-105">Para recuperar os dados de configuração em uma única chamada, use a função [**EnumPrinterDataEx**](enumprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="233c5-105">To retrieve the configuration data in a single call, use the [**EnumPrinterDataEx**](enumprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="233c5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="233c5-106">Syntax</span></span>


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="233c5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="233c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="233c5-108">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="233c5-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-109">Um identificador para a impressora cujos dados de configuração serão obtidos.</span><span class="sxs-lookup"><span data-stu-id="233c5-109">A handle to the printer whose configuration data is to be obtained.</span></span> <span data-ttu-id="233c5-110">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="233c5-110">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="233c5-111">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="233c5-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-112">Um valor de índice que especifica o valor dos dados de configuração a recuperar.</span><span class="sxs-lookup"><span data-stu-id="233c5-112">An index value that specifies the configuration data value to retrieve.</span></span>

<span data-ttu-id="233c5-113">Defina esse parâmetro como zero para a primeira chamada para **EnumPrinterData** para um identificador de impressora especificado.</span><span class="sxs-lookup"><span data-stu-id="233c5-113">Set this parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="233c5-114">Em seguida, aumente o parâmetro por um para chamadas subsequentes que envolvam a mesma impressora, até que a função retorne um erro \_ sem \_ mais \_ itens.</span><span class="sxs-lookup"><span data-stu-id="233c5-114">Then increment the parameter by one for subsequent calls involving the same printer, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="233c5-115">Consulte a seção de comentários a seguir para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="233c5-115">See the following Remarks section for further information.</span></span>

<span data-ttu-id="233c5-116">Se você usar a técnica mencionada nas descrições dos parâmetros *cbValueName* e *cbData* para obter valores de tamanho de buffer adequados, definindo esses parâmetros como zero em uma primeira chamada para **EnumPrinterData** para um identificador de impressora especificado, o valor de *dwIndex* não é importante para essa chamada.</span><span class="sxs-lookup"><span data-stu-id="233c5-116">If you use the technique mentioned in the descriptions of the *cbValueName* and *cbData* parameters to obtain adequate buffer size values, setting both those parameters to zero in a first call to **EnumPrinterData** for a specified printer handle, the value of *dwIndex* does not matter for that call.</span></span> <span data-ttu-id="233c5-117">Defina *dwIndex* como zero na próxima chamada para **EnumPrinterData** para iniciar o processo de enumeração real.</span><span class="sxs-lookup"><span data-stu-id="233c5-117">Set *dwIndex* to zero in the next call to **EnumPrinterData** to start the actual enumeration process.</span></span>

<span data-ttu-id="233c5-118">Os valores dos dados de configuração não são ordenados.</span><span class="sxs-lookup"><span data-stu-id="233c5-118">Configuration data values are not ordered.</span></span> <span data-ttu-id="233c5-119">Os novos valores terão um índice arbitrário.</span><span class="sxs-lookup"><span data-stu-id="233c5-119">New values will have an arbitrary index.</span></span> <span data-ttu-id="233c5-120">Isso significa que a função **EnumPrinterData** pode retornar valores em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="233c5-120">This means that the **EnumPrinterData** function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="233c5-121">*valores principais* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="233c5-121">*pValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-122">Um ponteiro para um buffer que recebe o nome do valor dos dados de configuração, incluindo um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="233c5-122">A pointer to a buffer that receives the name of the configuration data value, including a terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="233c5-123">*cbValueName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="233c5-123">*cbValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-124">O tamanho, em bytes, do buffer apontado por *valores* de datas.</span><span class="sxs-lookup"><span data-stu-id="233c5-124">The size, in bytes, of the buffer pointed to by *pValueName*.</span></span>

<span data-ttu-id="233c5-125">Se você quiser que o sistema operacional forneça um tamanho de buffer adequado, defina esse parâmetro e o parâmetro *cbData* como zero para a primeira chamada para **EnumPrinterData** para um identificador de impressora especificado.</span><span class="sxs-lookup"><span data-stu-id="233c5-125">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbData* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="233c5-126">Quando a função retornar, a variável apontada por *pcbValueName* conterá um tamanho de buffer grande o suficiente para enumerar com êxito todos os nomes de valor dos dados de configuração da impressora.</span><span class="sxs-lookup"><span data-stu-id="233c5-126">When the function returns, the variable pointed to by *pcbValueName* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="233c5-127">*pcbValueName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="233c5-127">*pcbValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-128">Um ponteiro para uma variável que recebe o número de bytes armazenados no buffer apontado por *valores* de número.</span><span class="sxs-lookup"><span data-stu-id="233c5-128">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pValueName*.</span></span>

</dd> <dt>

<span data-ttu-id="233c5-129">*pType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="233c5-129">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-130">Um ponteiro para uma variável que recebe um código que indica o tipo de dados armazenados no valor especificado.</span><span class="sxs-lookup"><span data-stu-id="233c5-130">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="233c5-131">Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="233c5-131">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span> <span data-ttu-id="233c5-132">O parâmetro *pType* poderá ser **nulo** se o código de tipo não for necessário.</span><span class="sxs-lookup"><span data-stu-id="233c5-132">The *pType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="233c5-133">*pData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="233c5-133">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-134">Um ponteiro para um buffer que recebe o valor dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="233c5-134">A pointer to a buffer that receives the configuration data value.</span></span>

<span data-ttu-id="233c5-135">Esse parâmetro poderá ser **nulo** se o valor dos dados de configuração não for necessário.</span><span class="sxs-lookup"><span data-stu-id="233c5-135">This parameter can be **NULL** if the configuration data value is not required.</span></span>

</dd> <dt>

<span data-ttu-id="233c5-136">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="233c5-136">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-137">O tamanho, em bytes, do buffer apontado por *pData*.</span><span class="sxs-lookup"><span data-stu-id="233c5-137">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="233c5-138">Se você quiser que o sistema operacional forneça um tamanho de buffer adequado, defina esse parâmetro e o parâmetro *cbValueName* como zero para a primeira chamada para **EnumPrinterData** para um identificador de impressora especificado.</span><span class="sxs-lookup"><span data-stu-id="233c5-138">If you want to have the operating system supply an adequate buffer size, set both this parameter and the *cbValueName* parameter to zero for the first call to **EnumPrinterData** for a specified printer handle.</span></span> <span data-ttu-id="233c5-139">Quando a função retornar, a variável apontada por *pcbData* conterá um tamanho de buffer grande o suficiente para enumerar com êxito todos os nomes de valor dos dados de configuração da impressora.</span><span class="sxs-lookup"><span data-stu-id="233c5-139">When the function returns, the variable pointed to by *pcbData* will contain a buffer size that is large enough to successfully enumerate all of the printer's configuration data value names.</span></span>

</dd> <dt>

<span data-ttu-id="233c5-140">*pcbData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="233c5-140">*pcbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="233c5-141">Um ponteiro para uma variável que recebe o número de bytes armazenados no buffer apontado por *pData*.</span><span class="sxs-lookup"><span data-stu-id="233c5-141">A pointer to a variable that receives the number of bytes stored into the buffer pointed to by *pData*.</span></span>

<span data-ttu-id="233c5-142">Esse parâmetro poderá ser **nulo** se *pData* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="233c5-142">This parameter can be **NULL** if *pData* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="233c5-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="233c5-143">Return value</span></span>

<span data-ttu-id="233c5-144">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="233c5-144">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="233c5-145">Se a função falhar, o valor de retorno será um código de erro do sistema.</span><span class="sxs-lookup"><span data-stu-id="233c5-145">If the function fails, the return value is a system error code.</span></span>

<span data-ttu-id="233c5-146">A função retorna \_ um erro sem \_ mais itens quando não há \_ mais valores de dados de configuração a serem recuperados para um identificador de impressora especificado.</span><span class="sxs-lookup"><span data-stu-id="233c5-146">The function returns ERROR\_NO\_MORE\_ITEMS when there are no more configuration data values to retrieve for a specified printer handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="233c5-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="233c5-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="233c5-148">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="233c5-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="233c5-149">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="233c5-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="233c5-150">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="233c5-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="233c5-151">**EnumPrinterData** recupera os dados de configuração da impressora definidos pela função [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="233c5-151">**EnumPrinterData** retrieves printer configuration data set by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="233c5-152">Os dados de configuração de uma impressora consistem em um conjunto de valores nomeados e digitados.</span><span class="sxs-lookup"><span data-stu-id="233c5-152">A printer's configuration data consists of a set of named and typed values.</span></span> <span data-ttu-id="233c5-153">A função **EnumPrinterData** Obtém um desses valores, e seu nome e um código de tipo, cada vez que você o chama.</span><span class="sxs-lookup"><span data-stu-id="233c5-153">The **EnumPrinterData** function obtains one of these values, and its name and a type code, each time you call it.</span></span> <span data-ttu-id="233c5-154">Chame a função **EnumPrinterData** várias vezes em sucessão para obter todos os valores de dados de configuração de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="233c5-154">Call the **EnumPrinterData** function several times in succession to obtain all of a printer's configuration data values.</span></span>

<span data-ttu-id="233c5-155">Os dados de configuração da impressora são armazenados no registro.</span><span class="sxs-lookup"><span data-stu-id="233c5-155">Printer configuration data is stored in the registry.</span></span> <span data-ttu-id="233c5-156">Ao enumerar os dados de configuração da impressora, você deve evitar chamar funções de registro que podem alterar esses dados.</span><span class="sxs-lookup"><span data-stu-id="233c5-156">While enumerating printer configuration data, you should avoid calling registry functions that might change that data.</span></span>

<span data-ttu-id="233c5-157">Se você quiser que o sistema operacional forneça um tamanho de buffer adequado, primeiro chame **EnumPrinterData** com os parâmetros *cbValueName* e *cbData* definidos como zero, conforme observado anteriormente na seção parâmetros.</span><span class="sxs-lookup"><span data-stu-id="233c5-157">If you want to have the operating system supply an adequate buffer size, first call **EnumPrinterData** with both the *cbValueName* and *cbData* parameters set to zero, as noted earlier in the Parameters section.</span></span> <span data-ttu-id="233c5-158">O valor de *dwIndex* não importa para essa chamada.</span><span class="sxs-lookup"><span data-stu-id="233c5-158">The value of *dwIndex* does not matter for this call.</span></span> <span data-ttu-id="233c5-159">Quando a função retornar, \* *pcbValueName* e \* *pcbData* conterá tamanhos de buffer grandes o suficiente para enumerar todos os nomes e valores de valores de dados de configuração da impressora.</span><span class="sxs-lookup"><span data-stu-id="233c5-159">When the function returns, \**pcbValueName* and \**pcbData* will contain buffer sizes that are large enough to enumerate all of the printer's configuration data value names and values.</span></span> <span data-ttu-id="233c5-160">Na próxima chamada, aloque o nome do valor e os buffers de dados, defina *cbValueName* e *cbData* para os tamanhos em bytes dos buffers alocados e defina *dwIndex* como zero.</span><span class="sxs-lookup"><span data-stu-id="233c5-160">On the next call, allocate value name and data buffers, set *cbValueName* and *cbData* to the sizes in bytes of the allocated buffers, and set *dwIndex* to zero.</span></span> <span data-ttu-id="233c5-161">Depois disso, continue a chamar a função **EnumPrinterData** , incrementando *dwIndex* por um a cada vez, até que a função retorne \_ um erro sem \_ mais \_ itens.</span><span class="sxs-lookup"><span data-stu-id="233c5-161">Thereafter, continue to call the **EnumPrinterData** function, incrementing *dwIndex* by one each time, until the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="requirements"></a><span data-ttu-id="233c5-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="233c5-162">Requirements</span></span>



| <span data-ttu-id="233c5-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="233c5-163">Requirement</span></span> | <span data-ttu-id="233c5-164">Valor</span><span class="sxs-lookup"><span data-stu-id="233c5-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="233c5-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="233c5-165">Minimum supported client</span></span><br/> | <span data-ttu-id="233c5-166">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="233c5-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="233c5-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="233c5-167">Minimum supported server</span></span><br/> | <span data-ttu-id="233c5-168">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="233c5-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="233c5-169">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="233c5-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="233c5-170"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="233c5-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="233c5-171">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="233c5-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="233c5-172"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="233c5-172"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="233c5-173">DLL</span><span class="sxs-lookup"><span data-stu-id="233c5-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="233c5-174"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="233c5-174"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="233c5-175">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="233c5-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="233c5-176">**EnumPrinterDataW** (Unicode) e **EnumPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="233c5-176">**EnumPrinterDataW** (Unicode) and **EnumPrinterDataA** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="233c5-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="233c5-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233c5-178">Impressão</span><span class="sxs-lookup"><span data-stu-id="233c5-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="233c5-179">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="233c5-179">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="233c5-180">**DeletePrinterData**</span><span class="sxs-lookup"><span data-stu-id="233c5-180">**DeletePrinterData**</span></span>](deleteprinterdata.md)
</dt> <dt>

[<span data-ttu-id="233c5-181">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="233c5-181">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="233c5-182">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="233c5-182">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="233c5-183">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="233c5-183">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="233c5-184">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="233c5-184">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="233c5-185">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="233c5-185">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> </dl>

 

