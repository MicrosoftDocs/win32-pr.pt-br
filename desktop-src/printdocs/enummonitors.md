---
description: A função EnumMonitors recupera informações sobre os monitores de porta instalados no servidor especificado.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: Função EnumMonitors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662122"
---
# <a name="enummonitors-function"></a><span data-ttu-id="1ee42-103">Função EnumMonitors</span><span class="sxs-lookup"><span data-stu-id="1ee42-103">EnumMonitors function</span></span>

<span data-ttu-id="1ee42-104">A função **EnumMonitors** recupera informações sobre os monitores de porta instalados no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="1ee42-104">The **EnumMonitors** function retrieves information about the port monitors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ee42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ee42-105">Syntax</span></span>


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="1ee42-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ee42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee42-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ee42-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee42-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual os monitores residem.</span><span class="sxs-lookup"><span data-stu-id="1ee42-108">A pointer to a null-terminated string that specifies the name of the server on which the monitors reside.</span></span> <span data-ttu-id="1ee42-109">Se esse parâmetro for **nulo**, os monitores locais serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="1ee42-109">If this parameter is **NULL**, the local monitors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="1ee42-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1ee42-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee42-111">A versão da estrutura apontada por *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="1ee42-111">The version of the structure pointed to by *pMonitors*.</span></span>

<span data-ttu-id="1ee42-112">Esse valor pode ser 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="1ee42-112">This value can be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1ee42-113">*pMonitors* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ee42-113">*pMonitors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee42-114">Um ponteiro para um buffer que recebe uma matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="1ee42-114">A pointer to a buffer that receives an array of structures.</span></span> <span data-ttu-id="1ee42-115">O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres referenciadas pelos membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="1ee42-115">The buffer must be large enough to store the strings referenced by the structure members.</span></span>

<span data-ttu-id="1ee42-116">Para determinar o tamanho do buffer necessário, chame **EnumMonitors** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="1ee42-116">To determine the required buffer size, call **EnumMonitors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="1ee42-117">**EnumMonitors** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="1ee42-117">**EnumMonitors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

<span data-ttu-id="1ee42-118">O buffer receberá uma matriz de estruturas de [**informações de monitor \_ \_ 1**](monitor-info-1.md) se o *nível* for 1 ou [**monitorará estruturas de \_ informações \_ 2**](monitor-info-2.md) se o *nível* for 2.</span><span class="sxs-lookup"><span data-stu-id="1ee42-118">The buffer receives an array of [**MONITOR\_INFO\_1**](monitor-info-1.md) structures if *Level* is 1, or [**MONITOR\_INFO\_2**](monitor-info-2.md) structures if *Level* is 2.</span></span>

</dd> <dt>

<span data-ttu-id="1ee42-119">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ee42-119">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee42-120">O tamanho, em bytes, do buffer apontado por *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="1ee42-120">The size, in bytes, of the buffer pointed to by *pMonitors*.</span></span>

</dd> <dt>

<span data-ttu-id="1ee42-121">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ee42-121">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee42-122">Um ponteiro para uma variável que recebe o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="1ee42-122">A pointer to a variable that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> <dt>

<span data-ttu-id="1ee42-123">*pcReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1ee42-123">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee42-124">Um ponteiro para uma variável que recebe o número de estruturas que foram retornadas no buffer apontado por *pMonitors*.</span><span class="sxs-lookup"><span data-stu-id="1ee42-124">A pointer to a variable that receives the number of structures that were returned in the buffer pointed to by *pMonitors*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee42-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ee42-125">Return value</span></span>

<span data-ttu-id="1ee42-126">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="1ee42-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="1ee42-127">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="1ee42-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ee42-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ee42-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1ee42-129">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="1ee42-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="1ee42-130">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1ee42-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="1ee42-131">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="1ee42-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1ee42-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ee42-132">Requirements</span></span>



| <span data-ttu-id="1ee42-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee42-133">Requirement</span></span> | <span data-ttu-id="1ee42-134">Valor</span><span class="sxs-lookup"><span data-stu-id="1ee42-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee42-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ee42-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee42-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ee42-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1ee42-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ee42-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee42-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1ee42-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1ee42-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1ee42-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee42-140"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee42-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1ee42-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ee42-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ee42-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ee42-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1ee42-143">DLL</span><span class="sxs-lookup"><span data-stu-id="1ee42-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ee42-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1ee42-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="1ee42-145">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1ee42-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1ee42-146">**EnumMonitorsW** (Unicode) e **EnumMonitorsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1ee42-146">**EnumMonitorsW** (Unicode) and **EnumMonitorsA** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="1ee42-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ee42-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee42-148">Impressão</span><span class="sxs-lookup"><span data-stu-id="1ee42-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1ee42-149">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="1ee42-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1ee42-150">**Informações do MONITOR \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="1ee42-150">**MONITOR\_INFO\_1**</span></span>](monitor-info-1.md)
</dt> <dt>

[<span data-ttu-id="1ee42-151">**Informações do MONITOR \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="1ee42-151">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

