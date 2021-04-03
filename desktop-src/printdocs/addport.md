---
description: A função AddPort adiciona o nome de uma porta à lista de portas com suporte. A função AddPort é exportada pelo monitor de porta.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: Função AddPort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837052"
---
# <a name="addport-function"></a><span data-ttu-id="15ceb-104">Função AddPort</span><span class="sxs-lookup"><span data-stu-id="15ceb-104">AddPort function</span></span>

<span data-ttu-id="15ceb-105">A função **AddPort** adiciona o nome de uma porta à lista de portas com suporte.</span><span class="sxs-lookup"><span data-stu-id="15ceb-105">The **AddPort** function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="15ceb-106">A função **AddPort** é exportada pelo monitor de porta.</span><span class="sxs-lookup"><span data-stu-id="15ceb-106">The **AddPort** function is exported by the port monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="15ceb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15ceb-107">Syntax</span></span>


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="15ceb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15ceb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15ceb-109">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15ceb-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ceb-110">Um ponteiro para uma cadeia de caracteres terminada em zero que especifica o nome do servidor ao qual a porta está conectada.</span><span class="sxs-lookup"><span data-stu-id="15ceb-110">A pointer to a zero-terminated string that specifies the name of the server to which the port is connected.</span></span> <span data-ttu-id="15ceb-111">Se esse parâmetro for **NULL**, a porta será local.</span><span class="sxs-lookup"><span data-stu-id="15ceb-111">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="15ceb-112">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15ceb-112">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ceb-113">Um identificador para a janela pai da caixa de diálogo **AddPort** .</span><span class="sxs-lookup"><span data-stu-id="15ceb-113">A handle to the parent window of the **AddPort** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="15ceb-114">*pMonitorName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15ceb-114">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ceb-115">Um ponteiro para uma cadeia de caracteres terminada em zero que especifica o monitor associado à porta.</span><span class="sxs-lookup"><span data-stu-id="15ceb-115">A pointer to a zero-terminated string that specifies the monitor associated with the port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15ceb-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15ceb-116">Return value</span></span>

<span data-ttu-id="15ceb-117">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="15ceb-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="15ceb-118">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="15ceb-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="15ceb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="15ceb-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="15ceb-120">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="15ceb-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="15ceb-121">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="15ceb-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="15ceb-122">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="15ceb-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="15ceb-123">A função **AddPort** procura a rede para localizar as portas existentes e exibe uma caixa de diálogo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="15ceb-123">The **AddPort** function browses the network to find existing ports, and displays a dialog box for the user.</span></span> <span data-ttu-id="15ceb-124">A função **AddPort** deve validar o nome da porta inserido pelo usuário chamando [**EnumPorts**](enumports.md) para garantir que não existam nomes duplicados.</span><span class="sxs-lookup"><span data-stu-id="15ceb-124">The **AddPort** function should validate the port name entered by the user by calling [**EnumPorts**](enumports.md) to ensure that no duplicate names exist.</span></span>

<span data-ttu-id="15ceb-125">O chamador da função **AddPort** deve ter acesso ao servidor para \_ \_ administrar o acesso ao servidor ao qual a porta está conectada.</span><span class="sxs-lookup"><span data-stu-id="15ceb-125">The caller of the **AddPort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="15ceb-126">Para adicionar uma porta sem exibir uma caixa de diálogo, chame a função **XcvData** em vez de **AddPort**.</span><span class="sxs-lookup"><span data-stu-id="15ceb-126">To add a port without displaying a dialog box, call the **XcvData** function instead of **AddPort**.</span></span> <span data-ttu-id="15ceb-127">Para obter mais informações sobre o **XcvData**, consulte o Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="15ceb-127">For more information about **XcvData**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="15ceb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15ceb-128">Requirements</span></span>



| <span data-ttu-id="15ceb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="15ceb-129">Requirement</span></span> | <span data-ttu-id="15ceb-130">Valor</span><span class="sxs-lookup"><span data-stu-id="15ceb-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15ceb-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15ceb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="15ceb-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15ceb-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15ceb-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15ceb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="15ceb-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15ceb-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15ceb-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="15ceb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="15ceb-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15ceb-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="15ceb-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15ceb-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="15ceb-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15ceb-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="15ceb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="15ceb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15ceb-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15ceb-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="15ceb-141">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="15ceb-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="15ceb-142">**AddPortW** (Unicode) e **addportaa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="15ceb-142">**AddPortW** (Unicode) and **AddPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="15ceb-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="15ceb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ceb-144">Impressão</span><span class="sxs-lookup"><span data-stu-id="15ceb-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="15ceb-145">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="15ceb-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="15ceb-146">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="15ceb-146">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="15ceb-147">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="15ceb-147">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="15ceb-148">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="15ceb-148">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




