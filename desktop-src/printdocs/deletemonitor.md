---
description: A função DeleteMonitor remove um monitor de porta adicionado pela função addmonitor.
ms.assetid: 32548d4f-830a-471d-8a72-c0f62f43ffa2
title: Função DeleteMonitor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMonitor
- DeleteMonitorA
- DeleteMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0f11504be516f79610200d4f7da9d571ae1cab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796139"
---
# <a name="deletemonitor-function"></a><span data-ttu-id="edad6-103">Função DeleteMonitor</span><span class="sxs-lookup"><span data-stu-id="edad6-103">DeleteMonitor function</span></span>

<span data-ttu-id="edad6-104">A função **DeleteMonitor** remove um monitor de porta adicionado pela função [**addmonitor**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="edad6-104">The **DeleteMonitor** function removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="edad6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edad6-105">Syntax</span></span>


```C++
BOOL DeleteMonitor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="edad6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edad6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edad6-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edad6-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edad6-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor do qual o monitor deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="edad6-108">A pointer to a null-terminated string that specifies the name of the server from which the monitor is to be removed.</span></span> <span data-ttu-id="edad6-109">Se esse parâmetro for **nulo**, o monitor de porta será removido localmente.</span><span class="sxs-lookup"><span data-stu-id="edad6-109">If this parameter is **NULL**, the port monitor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="edad6-110">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edad6-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edad6-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o monitor deve ser removido (por exemplo, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="edad6-111">A pointer to a null-terminated string that specifies the environment from which the monitor is to be removed (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="edad6-112">Se esse parâmetro for **nulo**, o monitor será removido do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão).</span><span class="sxs-lookup"><span data-stu-id="edad6-112">If this parameter is **NULL**, the monitor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="edad6-113">*pMonitorName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edad6-113">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edad6-114">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do monitor a ser removido.</span><span class="sxs-lookup"><span data-stu-id="edad6-114">A pointer to a null-terminated string that specifies the name of the monitor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edad6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="edad6-115">Return value</span></span>

<span data-ttu-id="edad6-116">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="edad6-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="edad6-117">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="edad6-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="edad6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="edad6-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="edad6-119">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="edad6-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="edad6-120">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="edad6-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="edad6-121">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="edad6-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="edad6-122">O chamador deve ter [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="edad6-122">The caller must have [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="edad6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edad6-123">Requirements</span></span>



| <span data-ttu-id="edad6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="edad6-124">Requirement</span></span> | <span data-ttu-id="edad6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="edad6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edad6-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edad6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="edad6-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="edad6-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="edad6-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edad6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="edad6-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="edad6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="edad6-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="edad6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="edad6-131"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edad6-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="edad6-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="edad6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="edad6-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="edad6-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="edad6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="edad6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edad6-135"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="edad6-135"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="edad6-136">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="edad6-136">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="edad6-137">**DeleteMonitorW** (Unicode) e **DeleteMonitorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="edad6-137">**DeleteMonitorW** (Unicode) and **DeleteMonitorA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="edad6-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="edad6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edad6-139">Impressão</span><span class="sxs-lookup"><span data-stu-id="edad6-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="edad6-140">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="edad6-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="edad6-141">**Addmonitor**</span><span class="sxs-lookup"><span data-stu-id="edad6-141">**AddMonitor**</span></span>](addmonitor.md)
</dt> </dl>

 

