---
description: A função EnumForms enumera os formulários com suporte na impressora especificada.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Função EnumForms (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296709"
---
# <a name="enumforms-function"></a><span data-ttu-id="e43a1-103">Função EnumForms</span><span class="sxs-lookup"><span data-stu-id="e43a1-103">EnumForms function</span></span>

<span data-ttu-id="e43a1-104">A função **EnumForms** enumera os formulários com suporte na impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="e43a1-104">The **EnumForms** function enumerates the forms supported by the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e43a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e43a1-105">Syntax</span></span>


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="e43a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e43a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e43a1-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e43a1-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e43a1-108">Identificador para a impressora para a qual os formulários devem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="e43a1-108">Handle to the printer for which the forms should be enumerated.</span></span> <span data-ttu-id="e43a1-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="e43a1-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="e43a1-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="e43a1-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e43a1-111">Especifica a versão da estrutura à qual o *pForm* aponta.</span><span class="sxs-lookup"><span data-stu-id="e43a1-111">Specifies the version of the structure to which *pForm* points.</span></span> <span data-ttu-id="e43a1-112">Esse valor deve ser 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="e43a1-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="e43a1-113">*pForm* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e43a1-113">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e43a1-114">Ponteiro para uma ou mais [**informações do formulário \_ \_ 1**](form-info-1.md) estruturas ou para uma ou mais estruturas de [**informações do formulário \_ \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="e43a1-114">Pointer to one or more [**FORM\_INFO\_1**](form-info-1.md) structures or to one or more [**FORM\_INFO\_2**](form-info-2.md) structures.</span></span> <span data-ttu-id="e43a1-115">Todas as estruturas terão o mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="e43a1-115">All the structures will have the same level.</span></span>

</dd> <dt>

<span data-ttu-id="e43a1-116">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e43a1-116">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e43a1-117">Especifica o tamanho, em bytes, do buffer para o qual *pForm* aponta.</span><span class="sxs-lookup"><span data-stu-id="e43a1-117">Specifies the size, in bytes, of the buffer to which *pForm* points.</span></span>

</dd> <dt>

<span data-ttu-id="e43a1-118">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e43a1-118">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e43a1-119">Ponteiro para uma variável que recebe o número de bytes copiados para a matriz para o qual *pForm* aponta (se a operação for bem-sucedida) ou o número de bytes necessários (se ele falhar porque *cbBuf* é muito pequeno).</span><span class="sxs-lookup"><span data-stu-id="e43a1-119">Pointer to a variable that receives the number of bytes copied to the array to which *pForm* points (if the operation succeeds) or the number of bytes required (if it fails because *cbBuf* is too small).</span></span>

</dd> <dt>

<span data-ttu-id="e43a1-120">*pcReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e43a1-120">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e43a1-121">Ponteiro para uma variável que recebe o número de estruturas copiadas na matriz para a qual *pForm* aponta.</span><span class="sxs-lookup"><span data-stu-id="e43a1-121">Pointer to a variable that receives the number of structures copied into the array to which *pForm* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e43a1-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e43a1-122">Return value</span></span>

<span data-ttu-id="e43a1-123">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e43a1-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e43a1-124">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="e43a1-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e43a1-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e43a1-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e43a1-126">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e43a1-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e43a1-127">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e43a1-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e43a1-128">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e43a1-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e43a1-129">Se o chamador for remoto e o *nível* for 2, o valor de **StringType** das estruturas [**\_ info \_ 2 do formulário**](form-info-2.md) retornado sempre será uma **cadeia de caracteres \_ LANGPAIR**.</span><span class="sxs-lookup"><span data-stu-id="e43a1-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) structures will always be **STRING\_LANGPAIR**.</span></span>

<span data-ttu-id="e43a1-130">No Windows Vista, os dados de formulário retornados pelo **EnumForms** são recuperados de um cache local quando o *hPrinter* refere-se a um servidor de impressão remoto ou a uma impressora hospedada por um servidor de impressão e há pelo menos uma conexão aberta com uma impressora no servidor de impressão remoto.</span><span class="sxs-lookup"><span data-stu-id="e43a1-130">In Windows Vista, the form data returned by **EnumForms** is retrieved from a local cache when *hPrinter* refers to a remote print server or a printer hosted by a print server and there is at least one open connection to a printer on the remote print server.</span></span> <span data-ttu-id="e43a1-131">Em todas as outras configurações, os dados do formulário são consultados do servidor de impressão remoto.</span><span class="sxs-lookup"><span data-stu-id="e43a1-131">In all other configurations, the form data is queried from the remote print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="e43a1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e43a1-132">Requirements</span></span>



| <span data-ttu-id="e43a1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e43a1-133">Requirement</span></span> | <span data-ttu-id="e43a1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e43a1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e43a1-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e43a1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e43a1-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e43a1-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e43a1-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e43a1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e43a1-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e43a1-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e43a1-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e43a1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e43a1-140"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e43a1-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e43a1-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e43a1-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="e43a1-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e43a1-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e43a1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e43a1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e43a1-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e43a1-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e43a1-145">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e43a1-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e43a1-146">**EnumFormsW** (Unicode) e **EnumFormsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e43a1-146">**EnumFormsW** (Unicode) and **EnumFormsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="e43a1-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e43a1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43a1-148">Impressão</span><span class="sxs-lookup"><span data-stu-id="e43a1-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e43a1-149">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e43a1-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e43a1-150">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="e43a1-150">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="e43a1-151">**Informações do formulário \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="e43a1-151">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="e43a1-152">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e43a1-152">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




