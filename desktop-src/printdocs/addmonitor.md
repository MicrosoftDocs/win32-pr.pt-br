---
description: A função addmonitor instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: Função addmonitor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011734"
---
# <a name="addmonitor-function"></a><span data-ttu-id="f4c38-103">Função addmonitor</span><span class="sxs-lookup"><span data-stu-id="f4c38-103">AddMonitor function</span></span>

<span data-ttu-id="f4c38-104">A função **addmonitor** instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="f4c38-104">The **AddMonitor** function installs a local port monitor and links the configuration, data, and monitor files.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4c38-105">Syntax</span></span>


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="f4c38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4c38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4c38-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4c38-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4c38-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o monitor deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="f4c38-108">A pointer to a null-terminated string that specifies the name of the server on which the monitor should be installed.</span></span> <span data-ttu-id="f4c38-109">Para sistemas que dão suporte apenas à instalação local de monitores, essa cadeia de caracteres deve ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="f4c38-109">For systems that support only local installation of monitors, this string should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f4c38-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f4c38-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4c38-111">A versão da estrutura à qual o *pMonitors* aponta.</span><span class="sxs-lookup"><span data-stu-id="f4c38-111">The version of the structure to which *pMonitors* points.</span></span> <span data-ttu-id="f4c38-112">Esse valor deve ser 2.</span><span class="sxs-lookup"><span data-stu-id="f4c38-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="f4c38-113">*pMonitors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f4c38-113">*pMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4c38-114">Um ponteiro para uma estrutura de [**informações do monitor \_ \_ 2**](monitor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c38-114">A pointer to a [**MONITOR\_INFO\_2**](monitor-info-2.md) structure.</span></span> <span data-ttu-id="f4c38-115">Se o membro **pEnvironment** da estrutura *pMonitors* for **NULL**, o ambiente atual do chamador (cliente), não do destino (servidor), será usado.</span><span class="sxs-lookup"><span data-stu-id="f4c38-115">If the **pEnvironment** member of the *pMonitors* structure is **NULL**, the current environment of the caller (client), not of the destination (server), is used.</span></span>

<span data-ttu-id="f4c38-116">Observe que a chamada falhará se o ambiente não corresponder ao ambiente do servidor, ou seja, você só poderá adicionar um monitor que foi gravado para a arquitetura do servidor.</span><span class="sxs-lookup"><span data-stu-id="f4c38-116">Note that the call will fail if the environment does not match the environment of the server, that is, you can only add a monitor that was written for the architecture of the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4c38-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4c38-117">Return value</span></span>

<span data-ttu-id="f4c38-118">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="f4c38-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f4c38-119">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="f4c38-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4c38-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4c38-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4c38-121">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f4c38-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f4c38-122">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4c38-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f4c38-123">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="f4c38-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f4c38-124">O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="f4c38-124">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="f4c38-125">Antes que um aplicativo chame a função **addmonitor** , todos os arquivos exigidos pelo monitor devem ser copiados para o diretório system32.</span><span class="sxs-lookup"><span data-stu-id="f4c38-125">Before an application calls the **AddMonitor** function, all files required by the monitor must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="f4c38-126">Para determinar os monitores de porta que estão instalados no momento, chame a função [**EnumMonitors**](enummonitors.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c38-126">To determine the port monitors that are currently installed, call the [**EnumMonitors**](enummonitors.md) function.</span></span>

<span data-ttu-id="f4c38-127">Para remover um monitor adicionado por **addmonitor**, chame a função [**DeleteMonitor**](deletemonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="f4c38-127">To remove a monitor added by **AddMonitor**, call the [**DeleteMonitor**](deletemonitor.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c38-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4c38-128">Requirements</span></span>



| <span data-ttu-id="f4c38-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4c38-129">Requirement</span></span> | <span data-ttu-id="f4c38-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f4c38-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c38-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4c38-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c38-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4c38-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f4c38-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4c38-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c38-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4c38-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f4c38-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f4c38-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4c38-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4c38-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f4c38-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4c38-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="f4c38-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4c38-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f4c38-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f4c38-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4c38-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f4c38-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f4c38-141">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f4c38-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f4c38-142">**AddMonitorW** (Unicode) e **addmonitora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f4c38-142">**AddMonitorW** (Unicode) and **AddMonitorA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="f4c38-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4c38-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c38-144">Impressão</span><span class="sxs-lookup"><span data-stu-id="f4c38-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f4c38-145">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="f4c38-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f4c38-146">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="f4c38-146">**DeleteMonitor**</span></span>](deletemonitor.md)
</dt> <dt>

[<span data-ttu-id="f4c38-147">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="f4c38-147">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="f4c38-148">**Informações do MONITOR \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f4c38-148">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

