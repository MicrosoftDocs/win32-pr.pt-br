---
description: A função EnumPorts enumera as portas que estão disponíveis para impressão em um servidor especificado.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: Função EnumPorts (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749689"
---
# <a name="enumports-function"></a><span data-ttu-id="462cb-103">Função EnumPorts</span><span class="sxs-lookup"><span data-stu-id="462cb-103">EnumPorts function</span></span>

<span data-ttu-id="462cb-104">A função **EnumPorts** enumera as portas que estão disponíveis para impressão em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="462cb-104">The **EnumPorts** function enumerates the ports that are available for printing on a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="462cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="462cb-105">Syntax</span></span>


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="462cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="462cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="462cb-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="462cb-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="462cb-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor cujas portas de impressora você deseja enumerar.</span><span class="sxs-lookup"><span data-stu-id="462cb-108">A pointer to a null-terminated string that specifies the name of the server whose printer ports you want to enumerate.</span></span>

<span data-ttu-id="462cb-109">Se *pname* for **nulo**, a função enumerará as portas de impressora do computador local.</span><span class="sxs-lookup"><span data-stu-id="462cb-109">If *pName* is **NULL**, the function enumerates the local machine's printer ports.</span></span>

</dd> <dt>

<span data-ttu-id="462cb-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="462cb-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="462cb-111">O tipo de informação retornado no buffer *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="462cb-111">The type of information returned in the *pPorts* buffer.</span></span> <span data-ttu-id="462cb-112">Se o *nível* for 1, *pPorts* receberá uma matriz de estruturas de [**informações de porta \_ \_ 1**](port-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="462cb-112">If *Level* is 1, *pPorts* receives an array of [**PORT\_INFO\_1**](port-info-1.md) structures.</span></span> <span data-ttu-id="462cb-113">Se o *nível* for 2, *pPorts* receberá uma matriz de estruturas de [**informações de porta \_ \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="462cb-113">If *Level* is 2, *pPorts* receives an array of [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="462cb-114">*pPorts* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="462cb-114">*pPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="462cb-115">Um ponteiro para um buffer que recebe uma matriz de estruturas de [**informações de porta \_ \_ 1**](port-info-1.md) ou de [**porta \_ \_ 2**](port-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="462cb-115">A pointer to a buffer that receives an array of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures.</span></span> <span data-ttu-id="462cb-116">Cada estrutura contém dados que descrevem uma porta de impressora disponível.</span><span class="sxs-lookup"><span data-stu-id="462cb-116">Each structure contains data that describes an available printer port.</span></span> <span data-ttu-id="462cb-117">O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres apontadas pelos membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="462cb-117">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="462cb-118">Para determinar o tamanho do buffer necessário, chame **EnumPorts** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="462cb-118">To determine the required buffer size, call **EnumPorts** with *cbBuf* set to zero.</span></span> <span data-ttu-id="462cb-119">**EnumPorts** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="462cb-119">**EnumPorts** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="462cb-120">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="462cb-120">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="462cb-121">O tamanho, em bytes, do buffer apontado por *pPorts*.</span><span class="sxs-lookup"><span data-stu-id="462cb-121">The size, in bytes, of the buffer pointed to by *pPorts*.</span></span>

</dd> <dt>

<span data-ttu-id="462cb-122">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="462cb-122">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="462cb-123">Um ponteiro para uma variável que recebe o número de bytes copiados para o buffer *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="462cb-123">A pointer to a variable that receives the number of bytes copied to the *pPorts* buffer.</span></span> <span data-ttu-id="462cb-124">Se o buffer for muito pequeno, a função falhará e a variável receberá o número de bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="462cb-124">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="462cb-125">*pcReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="462cb-125">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="462cb-126">Um ponteiro para uma variável que recebe o número de estruturas de informações de [**porta \_ \_ 1**](port-info-1.md) ou [**informações de porta \_ \_ 2**](port-info-2.md) retornadas no buffer *pPorts* .</span><span class="sxs-lookup"><span data-stu-id="462cb-126">A pointer to a variable that receives the number of [**PORT\_INFO\_1**](port-info-1.md) or [**PORT\_INFO\_2**](port-info-2.md) structures returned in the *pPorts* buffer.</span></span> <span data-ttu-id="462cb-127">Este é o número de portas de impressora que estão disponíveis no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="462cb-127">This is the number of printer ports that are available on the specified server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="462cb-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="462cb-128">Return value</span></span>

<span data-ttu-id="462cb-129">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="462cb-129">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="462cb-130">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="462cb-130">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="462cb-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="462cb-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="462cb-132">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="462cb-132">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="462cb-133">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="462cb-133">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="462cb-134">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="462cb-134">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="462cb-135">A função **EnumPorts** pode ter sucesso mesmo que o servidor especificado por *pname* não tenha uma impressora definida.</span><span class="sxs-lookup"><span data-stu-id="462cb-135">The **EnumPorts** function can succeed even if the server specified by *pName* does not have a printer defined.</span></span>

## <a name="requirements"></a><span data-ttu-id="462cb-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="462cb-136">Requirements</span></span>



| <span data-ttu-id="462cb-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="462cb-137">Requirement</span></span> | <span data-ttu-id="462cb-138">Valor</span><span class="sxs-lookup"><span data-stu-id="462cb-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462cb-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="462cb-139">Minimum supported client</span></span><br/> | <span data-ttu-id="462cb-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="462cb-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="462cb-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="462cb-141">Minimum supported server</span></span><br/> | <span data-ttu-id="462cb-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="462cb-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="462cb-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="462cb-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="462cb-144"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="462cb-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="462cb-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="462cb-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="462cb-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="462cb-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="462cb-147">DLL</span><span class="sxs-lookup"><span data-stu-id="462cb-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="462cb-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="462cb-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="462cb-149">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="462cb-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="462cb-150">**EnumPortsW** (Unicode) e **EnumPortsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="462cb-150">**EnumPortsW** (Unicode) and **EnumPortsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="462cb-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="462cb-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="462cb-152">Impressão</span><span class="sxs-lookup"><span data-stu-id="462cb-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="462cb-153">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="462cb-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="462cb-154">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="462cb-154">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="462cb-155">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="462cb-155">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="462cb-156">**Informações da porta \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="462cb-156">**PORT\_INFO\_1**</span></span>](port-info-1.md)
</dt> <dt>

[<span data-ttu-id="462cb-157">**Informações da porta \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="462cb-157">**PORT\_INFO\_2**</span></span>](port-info-2.md)
</dt> </dl>

 

