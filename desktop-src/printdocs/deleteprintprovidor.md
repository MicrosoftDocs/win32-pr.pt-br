---
description: A função DeletePrintProvidor remove um provedor de impressão adicionado pela função AddPrintProvidor.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: Função DeletePrintProvidor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170360"
---
# <a name="deleteprintprovidor-function"></a><span data-ttu-id="29912-103">Função DeletePrintProvidor</span><span class="sxs-lookup"><span data-stu-id="29912-103">DeletePrintProvidor function</span></span>

<span data-ttu-id="29912-104">A função **DeletePrintProvidor** remove um provedor de impressão adicionado pela função [**AddPrintProvidor**](addprintprovidor.md) .</span><span class="sxs-lookup"><span data-stu-id="29912-104">The **DeletePrintProvidor** function removes a print provider added by the [**AddPrintProvidor**](addprintprovidor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="29912-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29912-105">Syntax</span></span>


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a><span data-ttu-id="29912-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29912-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29912-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29912-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29912-108">Reservado deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="29912-108">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="29912-109">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29912-109">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29912-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o provedor deve ser removido (por exemplo, Windows NT x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="29912-110">A pointer to a null-terminated string that specifies the environment from which the provider is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="29912-111">Se esse parâmetro for **nulo**, o provedor será removido do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão).</span><span class="sxs-lookup"><span data-stu-id="29912-111">If this parameter is **NULL**, the provider is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="29912-112">**NULL** é o valor recomendado porque fornece a portabilidade máxima.</span><span class="sxs-lookup"><span data-stu-id="29912-112">**NULL** is the recommended value because it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="29912-113">*pPrintProviderName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29912-113">*pPrintProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29912-114">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do provedor a ser removido.</span><span class="sxs-lookup"><span data-stu-id="29912-114">A pointer to a null-terminated string that specifies the name of the provider to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29912-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29912-115">Return value</span></span>

<span data-ttu-id="29912-116">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="29912-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="29912-117">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="29912-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="29912-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="29912-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="29912-119">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="29912-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="29912-120">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="29912-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="29912-121">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="29912-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29912-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29912-122">Requirements</span></span>



| <span data-ttu-id="29912-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="29912-123">Requirement</span></span> | <span data-ttu-id="29912-124">Valor</span><span class="sxs-lookup"><span data-stu-id="29912-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29912-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29912-125">Minimum supported client</span></span><br/> | <span data-ttu-id="29912-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="29912-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="29912-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29912-127">Minimum supported server</span></span><br/> | <span data-ttu-id="29912-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="29912-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="29912-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="29912-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="29912-130"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29912-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="29912-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29912-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="29912-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29912-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="29912-133">DLL</span><span class="sxs-lookup"><span data-stu-id="29912-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29912-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="29912-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="29912-135">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="29912-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="29912-136">**DeletePrintProvidorW** (Unicode) e **DeletePrintProvidorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="29912-136">**DeletePrintProvidorW** (Unicode) and **DeletePrintProvidorA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="29912-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="29912-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29912-138">Impressão</span><span class="sxs-lookup"><span data-stu-id="29912-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="29912-139">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="29912-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="29912-140">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="29912-140">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




