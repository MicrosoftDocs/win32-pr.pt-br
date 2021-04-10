---
description: Recupera o GUID, a versão e a data dos drivers de impressora de núcleo especificados e o caminho para seus pacotes.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Função GetCorePrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296706"
---
# <a name="getcoreprinterdrivers-function"></a><span data-ttu-id="58fdd-103">Função GetCorePrinterDrivers</span><span class="sxs-lookup"><span data-stu-id="58fdd-103">GetCorePrinterDrivers function</span></span>

<span data-ttu-id="58fdd-104">Recupera o GUID, a versão e a data dos drivers de impressora de núcleo especificados e o caminho para seus pacotes.</span><span class="sxs-lookup"><span data-stu-id="58fdd-104">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span>

## <a name="syntax"></a><span data-ttu-id="58fdd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58fdd-105">Syntax</span></span>


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a><span data-ttu-id="58fdd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58fdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58fdd-107">*pszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="58fdd-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fdd-108">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="58fdd-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="58fdd-109">Use **NULL** para o computador local.</span><span class="sxs-lookup"><span data-stu-id="58fdd-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="58fdd-110">*pszEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="58fdd-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fdd-111">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador (por exemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="58fdd-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="58fdd-112">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="58fdd-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="58fdd-113">*pszzCoreDriverDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="58fdd-113">*pszzCoreDriverDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fdd-114">Um ponteiro para uma cadeia de caracteres múltipla terminada em nulo que especifica os GUIDs dos drivers da impressora principal.</span><span class="sxs-lookup"><span data-stu-id="58fdd-114">A pointer to a null-terminated multi-string that specifies the GUIDs of the core printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="58fdd-115">*cCorePrinterDrivers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="58fdd-115">*cCorePrinterDrivers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58fdd-116">O número de cadeias de caracteres em *pszzCoreDriverDependencies*.</span><span class="sxs-lookup"><span data-stu-id="58fdd-116">The number of strings in *pszzCoreDriverDependencies*.</span></span>

</dd> <dt>

<span data-ttu-id="58fdd-117">*pCorePrinterDrivers* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="58fdd-117">*pCorePrinterDrivers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58fdd-118">Um ponteiro para uma matriz de uma ou mais estruturas de [**\_ \_ Driver de impressora principal**](core-printer-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="58fdd-118">A pointer to an array of one or more [**CORE\_PRINTER\_DRIVER**](core-printer-driver.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58fdd-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58fdd-119">Return value</span></span>

<span data-ttu-id="58fdd-120">Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="58fdd-120">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="58fdd-121">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="58fdd-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="58fdd-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="58fdd-122">Remarks</span></span>

<span data-ttu-id="58fdd-123">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="58fdd-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="58fdd-124">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="58fdd-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="58fdd-125">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="58fdd-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

## <a name="requirements"></a><span data-ttu-id="58fdd-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58fdd-126">Requirements</span></span>



| <span data-ttu-id="58fdd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="58fdd-127">Requirement</span></span> | <span data-ttu-id="58fdd-128">Valor</span><span class="sxs-lookup"><span data-stu-id="58fdd-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58fdd-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58fdd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="58fdd-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58fdd-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="58fdd-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58fdd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="58fdd-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="58fdd-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="58fdd-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58fdd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="58fdd-134"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58fdd-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="58fdd-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58fdd-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="58fdd-136"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58fdd-136"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="58fdd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="58fdd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58fdd-138"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58fdd-138"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="58fdd-139">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="58fdd-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="58fdd-140">**GetCorePrinterDriversW** (Unicode) e **GetCorePrinterDriversA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="58fdd-140">**GetCorePrinterDriversW** (Unicode) and **GetCorePrinterDriversA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="58fdd-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="58fdd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58fdd-142">Impressão</span><span class="sxs-lookup"><span data-stu-id="58fdd-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="58fdd-143">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="58fdd-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

