---
description: A função DeletePort exibe uma caixa de diálogo que permite ao usuário excluir um nome de porta.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: Função DeletePort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170361"
---
# <a name="deleteport-function"></a><span data-ttu-id="0b2b8-103">Função DeletePort</span><span class="sxs-lookup"><span data-stu-id="0b2b8-103">DeletePort function</span></span>

<span data-ttu-id="0b2b8-104">A função **DeletePort** exibe uma caixa de diálogo que permite ao usuário excluir um nome de porta.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-104">The **DeletePort** function displays a dialog box that allows the user to delete a port name.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b2b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b2b8-105">Syntax</span></span>


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="0b2b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b2b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b2b8-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b2b8-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b2b8-108">Um ponteiro para uma cadeia de caracteres terminada em zero que especifica o nome do servidor para o qual a porta deve ser excluída.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-108">A pointer to a zero-terminated string that specifies the name of the server for which the port should be deleted.</span></span> <span data-ttu-id="0b2b8-109">Se esse parâmetro for **NULL**, uma porta local será excluída.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-109">If this parameter is **NULL**, a local port is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="0b2b8-110">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b2b8-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b2b8-111">Um identificador para a janela pai da caixa de diálogo de exclusão de porta.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-111">A handle to the parent window of the port-deletion dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="0b2b8-112">*pPortName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0b2b8-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b2b8-113">Um ponteiro para uma cadeia de caracteres terminada em zero que especifica o nome da porta que deve ser excluída.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-113">A pointer to a zero-terminated string that specifies the name of the port that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b2b8-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b2b8-114">Return value</span></span>

<span data-ttu-id="0b2b8-115">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="0b2b8-116">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b2b8-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b2b8-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0b2b8-118">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0b2b8-119">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0b2b8-120">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="0b2b8-121">Um aplicativo pode recuperar os nomes de portas válidas chamando a função [**EnumPorts**](enumports.md) .</span><span class="sxs-lookup"><span data-stu-id="0b2b8-121">An application can retrieve the names of valid ports by calling the [**EnumPorts**](enumports.md) function.</span></span>

<span data-ttu-id="0b2b8-122">A função **DeletePort** retornará um erro se uma impressora estiver conectada à porta especificada no momento.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-122">The **DeletePort** function returns an error if a printer is currently connected to the specified port.</span></span>

<span data-ttu-id="0b2b8-123">O chamador da função **DeletePort** deve ter acesso ao servidor para \_ \_ administrar o acesso ao servidor ao qual a porta está conectada.</span><span class="sxs-lookup"><span data-stu-id="0b2b8-123">The caller of the **DeletePort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b2b8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b2b8-124">Requirements</span></span>



| <span data-ttu-id="0b2b8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b2b8-125">Requirement</span></span> | <span data-ttu-id="0b2b8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0b2b8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2b8-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b2b8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0b2b8-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b2b8-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0b2b8-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b2b8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0b2b8-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0b2b8-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0b2b8-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0b2b8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b2b8-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b2b8-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0b2b8-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b2b8-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b2b8-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b2b8-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0b2b8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0b2b8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b2b8-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0b2b8-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0b2b8-137">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0b2b8-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0b2b8-138">**DeletePortW** (Unicode) e **DeletePortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0b2b8-138">**DeletePortW** (Unicode) and **DeletePortA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="0b2b8-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b2b8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b2b8-140">Impressão</span><span class="sxs-lookup"><span data-stu-id="0b2b8-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0b2b8-141">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="0b2b8-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0b2b8-142">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="0b2b8-142">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="0b2b8-143">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="0b2b8-143">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




