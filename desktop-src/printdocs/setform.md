---
description: A função setform define as informações do formulário para a impressora especificada.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: Função SetFormat (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296705"
---
# <a name="setform-function"></a><span data-ttu-id="b6e56-103">Função SetFormat</span><span class="sxs-lookup"><span data-stu-id="b6e56-103">SetForm function</span></span>

<span data-ttu-id="b6e56-104">A função **setform** define as informações do formulário para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="b6e56-104">The **SetForm** function sets the form information for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6e56-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6e56-105">Syntax</span></span>


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a><span data-ttu-id="b6e56-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6e56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6e56-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6e56-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e56-108">Um identificador para a impressora para a qual as informações do formulário estão definidas.</span><span class="sxs-lookup"><span data-stu-id="b6e56-108">A handle to the printer for which the form information is set.</span></span> <span data-ttu-id="b6e56-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="b6e56-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="b6e56-110">*pFormName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6e56-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e56-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do formulário para o qual as informações do formulário são definidas.</span><span class="sxs-lookup"><span data-stu-id="b6e56-111">A pointer to a null-terminated string that specifies the form name for which the form information is set.</span></span>

</dd> <dt>

<span data-ttu-id="b6e56-112">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b6e56-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e56-113">A versão da estrutura à qual o *pForm* aponta.</span><span class="sxs-lookup"><span data-stu-id="b6e56-113">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="b6e56-114">Esse valor deve ser 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="b6e56-114">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b6e56-115">*pForm* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6e56-115">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6e56-116">Um ponteiro para uma estrutura de [**informações de formulário \_ \_ 1**](form-info-1.md) ou de [**formulário \_ \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="b6e56-116">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6e56-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6e56-117">Return value</span></span>

<span data-ttu-id="b6e56-118">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b6e56-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b6e56-119">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="b6e56-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6e56-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6e56-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b6e56-121">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b6e56-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b6e56-122">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b6e56-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b6e56-123">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="b6e56-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b6e56-124">**SetFormat** pode ser chamado várias vezes para uma [**informação de formulário \_ \_ 2**](form-info-2.md)existente, cada chamada adiciona pares adicionais de valores **pDisplayName** e **wLangId** .</span><span class="sxs-lookup"><span data-stu-id="b6e56-124">**SetForm** can be called multiple times for an existing [**FORM\_INFO\_2**](form-info-2.md), each call adding additional pairs of **pDisplayName** and **wLangId** values.</span></span> <span data-ttu-id="b6e56-125">Todas as versões de idiomas do formulário obterão os valores de **tamanho** e **ImageableArea** do **formulário \_ informações \_ 2** na chamada mais recente para **setform**.</span><span class="sxs-lookup"><span data-stu-id="b6e56-125">All languages versions of the form will get the **Size** and **ImageableArea** values of the **FORM\_INFO\_2** in the most recent call to **SetForm**.</span></span>

<span data-ttu-id="b6e56-126">Se o chamador for remoto e o *nível* for 2, o valor de **StringType** do [**formulário \_ info \_ 2**](form-info-2.md) não poderá ser String \_ MUIDLL.</span><span class="sxs-lookup"><span data-stu-id="b6e56-126">If the caller is remote and the *Level* is 2, the **StringType** value of the [**FORM\_INFO\_2**](form-info-2.md) cannot be STRING\_MUIDLL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6e56-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6e56-127">Requirements</span></span>



| <span data-ttu-id="b6e56-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6e56-128">Requirement</span></span> | <span data-ttu-id="b6e56-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b6e56-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6e56-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6e56-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b6e56-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b6e56-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b6e56-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6e56-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b6e56-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b6e56-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b6e56-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b6e56-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6e56-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6e56-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b6e56-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6e56-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6e56-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6e56-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b6e56-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b6e56-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6e56-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b6e56-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b6e56-140">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b6e56-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b6e56-141">**SetFormW** (Unicode) e **setformaa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b6e56-141">**SetFormW** (Unicode) and **SetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="b6e56-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6e56-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6e56-143">Impressão</span><span class="sxs-lookup"><span data-stu-id="b6e56-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b6e56-144">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="b6e56-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b6e56-145">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="b6e56-145">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="b6e56-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b6e56-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="b6e56-147">**Informações do formulário \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b6e56-147">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="b6e56-148">**Informações do formulário \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b6e56-148">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> </dl>

 

 




