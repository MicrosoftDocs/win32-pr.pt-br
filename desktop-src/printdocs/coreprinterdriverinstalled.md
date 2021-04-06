---
description: A função CorePrinterDriverInstalled relata se um driver de impressora principal com um GUID, uma data e uma versão especificados estão instalados.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Função CorePrinterDriverInstalled (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011394"
---
# <a name="coreprinterdriverinstalled-function"></a><span data-ttu-id="b0790-103">Função CorePrinterDriverInstalled</span><span class="sxs-lookup"><span data-stu-id="b0790-103">CorePrinterDriverInstalled function</span></span>

<span data-ttu-id="b0790-104">A função **CorePrinterDriverInstalled** relata se um driver de impressora principal com um GUID, uma data e uma versão especificados estão instalados.</span><span class="sxs-lookup"><span data-stu-id="b0790-104">The **CorePrinterDriverInstalled** function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0790-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0790-105">Syntax</span></span>


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="b0790-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0790-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0790-107">*pszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0790-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0790-108">Ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="b0790-108">Pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="b0790-109">Use **NULL** para o computador local.</span><span class="sxs-lookup"><span data-stu-id="b0790-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="b0790-110">*pszEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0790-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0790-111">Ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador (por exemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="b0790-111">Pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="b0790-112">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b0790-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b0790-113">*CoreDriverGUID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0790-113">*CoreDriverGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0790-114">O GUID do driver de impressora principal.</span><span class="sxs-lookup"><span data-stu-id="b0790-114">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="b0790-115">*ftDriverDate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0790-115">*ftDriverDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0790-116">A data do driver de impressora principal.</span><span class="sxs-lookup"><span data-stu-id="b0790-116">The date of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="b0790-117">*dwlDriverVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0790-117">*dwlDriverVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0790-118">A versão do driver de impressora principal.</span><span class="sxs-lookup"><span data-stu-id="b0790-118">The version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="b0790-119">*pbDriverInstalled* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0790-119">*pbDriverInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0790-120">Um ponteiro para **verdadeiro** se o driver ou uma versão mais recente estiver instalado; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="b0790-120">A pointer to **TRUE** if the driver, or a newer version, is installed, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0790-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0790-121">Return value</span></span>

<span data-ttu-id="b0790-122">Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="b0790-122">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="b0790-123">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="b0790-123">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0790-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0790-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b0790-125">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b0790-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b0790-126">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b0790-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b0790-127">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="b0790-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b0790-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0790-128">Requirements</span></span>



| <span data-ttu-id="b0790-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0790-129">Requirement</span></span> | <span data-ttu-id="b0790-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b0790-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0790-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0790-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b0790-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0790-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b0790-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0790-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b0790-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b0790-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0790-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0790-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0790-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0790-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b0790-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0790-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0790-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0790-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b0790-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b0790-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0790-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0790-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="b0790-141">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b0790-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b0790-142">**CorePrinterDriverInstalledW** (Unicode) e **CorePrinterDriverInstalledA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b0790-142">**CorePrinterDriverInstalledW** (Unicode) and **CorePrinterDriverInstalledA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b0790-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0790-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0790-144">Impressão</span><span class="sxs-lookup"><span data-stu-id="b0790-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b0790-145">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="b0790-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

