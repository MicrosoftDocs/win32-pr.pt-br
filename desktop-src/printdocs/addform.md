---
description: A função AddFormat adiciona um formulário à lista de formulários disponíveis que podem ser selecionados para a impressora especificada.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: Função AddFormat (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810639"
---
# <a name="addform-function"></a><span data-ttu-id="9ff6e-103">Função AddFormat</span><span class="sxs-lookup"><span data-stu-id="9ff6e-103">AddForm function</span></span>

<span data-ttu-id="9ff6e-104">A função **AddFormat** adiciona um formulário à lista de formulários disponíveis que podem ser selecionados para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-104">The **AddForm** function adds a form to the list of available forms that can be selected for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff6e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ff6e-105">Syntax</span></span>


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a><span data-ttu-id="9ff6e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ff6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff6e-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ff6e-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff6e-108">Um identificador para a impressora que dá suporte à impressão com o formulário especificado.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-108">A handle to the printer that supports printing with the specified form.</span></span> <span data-ttu-id="9ff6e-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9ff6e-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff6e-111">O nível da estrutura à qual *pForm* aponta.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-111">The level of the structure to which *pForm* points.</span></span> <span data-ttu-id="9ff6e-112">Esse valor deve ser 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-113">*pForm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ff6e-113">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ff6e-114">Um ponteiro para uma estrutura de [**informações de formulário \_ \_ 1**](form-info-1.md) ou de [**formulário \_ \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff6e-114">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff6e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ff6e-115">Return value</span></span>

<span data-ttu-id="9ff6e-116">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9ff6e-117">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff6e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ff6e-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9ff6e-119">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9ff6e-120">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9ff6e-121">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9ff6e-122">Um aplicativo pode determinar quais formulários estão disponíveis para uma impressora chamando a função [**EnumForms**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff6e-122">An application can determine which forms are available for a printer by calling the [**EnumForms**](enumforms.md) function.</span></span>

<span data-ttu-id="9ff6e-123">Se *pForm* apontar para uma [**informação de formulário \_ \_ 2**](form-info-2.md), o **AddForm** falhará se um formulário com o nome especificado já existir ou se o valor de *pKeyword* da estrutura já existir.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-123">If *pForm* points to a [**FORM\_INFO\_2**](form-info-2.md), then **AddForm** will fail if either a form with the specified name already exists or the structure's *pKeyword* value already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff6e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ff6e-124">Requirements</span></span>



| <span data-ttu-id="9ff6e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ff6e-125">Requirement</span></span> | <span data-ttu-id="9ff6e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="9ff6e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff6e-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ff6e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff6e-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ff6e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ff6e-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ff6e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff6e-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9ff6e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ff6e-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9ff6e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff6e-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ff6e-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9ff6e-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ff6e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ff6e-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ff6e-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9ff6e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff6e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff6e-136"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff6e-136"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="9ff6e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ff6e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff6e-138">Impressão</span><span class="sxs-lookup"><span data-stu-id="9ff6e-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-139">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="9ff6e-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-140">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-140">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-141">**Informações do formulário \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-141">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-142">**Informações do formulário \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-142">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> <dt>

[<span data-ttu-id="9ff6e-143">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-143">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




