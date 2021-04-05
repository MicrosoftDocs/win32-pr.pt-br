---
description: A função ConfigurePort exibe a caixa de diálogo porta-configuração de uma porta no servidor especificado.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Função ConfigurePort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921684"
---
# <a name="configureport-function"></a><span data-ttu-id="94838-103">Função ConfigurePort</span><span class="sxs-lookup"><span data-stu-id="94838-103">ConfigurePort function</span></span>

<span data-ttu-id="94838-104">A função **ConfigurePort** exibe a caixa de diálogo porta-configuração de uma porta no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="94838-104">The **ConfigurePort** function displays the port-configuration dialog box for a port on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="94838-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94838-105">Syntax</span></span>


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="94838-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94838-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94838-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94838-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94838-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual a porta especificada existe.</span><span class="sxs-lookup"><span data-stu-id="94838-108">Pointer to a null-terminated string that specifies the name of the server on which the specified port exists.</span></span> <span data-ttu-id="94838-109">Se esse parâmetro for **NULL**, a porta será local.</span><span class="sxs-lookup"><span data-stu-id="94838-109">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="94838-110">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94838-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94838-111">Identificador para a janela pai da caixa de diálogo porta-configuração.</span><span class="sxs-lookup"><span data-stu-id="94838-111">Handle to the parent window of the port-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="94838-112">*pPortName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="94838-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94838-113">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da porta a ser configurada.</span><span class="sxs-lookup"><span data-stu-id="94838-113">Pointer to a null-terminated string that specifies the name of the port to be configured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94838-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94838-114">Return value</span></span>

<span data-ttu-id="94838-115">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="94838-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="94838-116">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="94838-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="94838-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="94838-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="94838-118">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="94838-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="94838-119">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94838-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="94838-120">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="94838-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="94838-121">Antes de chamar a função **ConfigurePort** , um aplicativo deve chamar a função [**EnumPorts**](enumports.md) para determinar nomes de porta válidos.</span><span class="sxs-lookup"><span data-stu-id="94838-121">Before calling the **ConfigurePort** function, an application should call the [**EnumPorts**](enumports.md) function to determine valid port names.</span></span>

## <a name="requirements"></a><span data-ttu-id="94838-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94838-122">Requirements</span></span>



| <span data-ttu-id="94838-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="94838-123">Requirement</span></span> | <span data-ttu-id="94838-124">Valor</span><span class="sxs-lookup"><span data-stu-id="94838-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94838-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94838-125">Minimum supported client</span></span><br/> | <span data-ttu-id="94838-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94838-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="94838-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94838-127">Minimum supported server</span></span><br/> | <span data-ttu-id="94838-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="94838-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="94838-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="94838-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="94838-130"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94838-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="94838-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94838-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="94838-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94838-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="94838-133">DLL</span><span class="sxs-lookup"><span data-stu-id="94838-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94838-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="94838-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="94838-135">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="94838-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="94838-136">**ConfigurePortW** (Unicode) e **ConfigurePortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="94838-136">**ConfigurePortW** (Unicode) and **ConfigurePortA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="94838-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="94838-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94838-138">Impressão</span><span class="sxs-lookup"><span data-stu-id="94838-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="94838-139">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="94838-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="94838-140">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="94838-140">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




