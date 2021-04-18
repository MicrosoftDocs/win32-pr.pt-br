---
description: A função GetPrinterDriverDirectory recupera o caminho do diretório do driver de impressora.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: Função GetPrinterDriverDirectory (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807793"
---
# <a name="getprinterdriverdirectory-function"></a><span data-ttu-id="a13d8-103">Função GetPrinterDriverDirectory</span><span class="sxs-lookup"><span data-stu-id="a13d8-103">GetPrinterDriverDirectory function</span></span>

<span data-ttu-id="a13d8-104">A função **GetPrinterDriverDirectory** recupera o caminho do diretório do driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="a13d8-104">The **GetPrinterDriverDirectory** function retrieves the path of the printer-driver directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a13d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a13d8-105">Syntax</span></span>


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="a13d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a13d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a13d8-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o driver de impressora reside.</span><span class="sxs-lookup"><span data-stu-id="a13d8-108">A pointer to a null-terminated string that specifies the name of the server on which the printer driver resides.</span></span> <span data-ttu-id="a13d8-109">Se esse parâmetro for **NULL**, o caminho do diretório do driver local será recuperado.</span><span class="sxs-lookup"><span data-stu-id="a13d8-109">If this parameter is **NULL**, the local driver-directory path is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="a13d8-110">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a13d8-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="a13d8-112">Se esse parâmetro for **NULL**, o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.</span><span class="sxs-lookup"><span data-stu-id="a13d8-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="a13d8-113">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-114">O nível da estrutura.</span><span class="sxs-lookup"><span data-stu-id="a13d8-114">The structure level.</span></span> <span data-ttu-id="a13d8-115">Esse valor deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="a13d8-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="a13d8-116">*pDriverDirectory* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-116">*pDriverDirectory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-117">Um ponteiro para um buffer que recebe o caminho.</span><span class="sxs-lookup"><span data-stu-id="a13d8-117">A pointer to a buffer that receives the path.</span></span>

</dd> <dt>

<span data-ttu-id="a13d8-118">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-119">O tamanho do buffer para o qual *pDriverDirectory* aponta.</span><span class="sxs-lookup"><span data-stu-id="a13d8-119">The size of the buffer to which *pDriverDirectory* points.</span></span>

</dd> <dt>

<span data-ttu-id="a13d8-120">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a13d8-121">Um ponteiro para um valor que especifica o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="a13d8-121">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a13d8-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a13d8-122">Return value</span></span>

<span data-ttu-id="a13d8-123">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a13d8-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a13d8-124">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="a13d8-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a13d8-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a13d8-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a13d8-126">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="a13d8-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a13d8-127">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a13d8-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a13d8-128">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="a13d8-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a13d8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a13d8-129">Requirements</span></span>



| <span data-ttu-id="a13d8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a13d8-130">Requirement</span></span> | <span data-ttu-id="a13d8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a13d8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a13d8-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a13d8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a13d8-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a13d8-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a13d8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a13d8-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a13d8-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a13d8-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a13d8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a13d8-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a13d8-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a13d8-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a13d8-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="a13d8-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a13d8-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a13d8-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a13d8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a13d8-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a13d8-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a13d8-142">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a13d8-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a13d8-143">**GetPrinterDriverDirectoryW** (Unicode) e **GetPrinterDriverDirectoryA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a13d8-143">**GetPrinterDriverDirectoryW** (Unicode) and **GetPrinterDriverDirectoryA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a13d8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="a13d8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a13d8-145">Impressão</span><span class="sxs-lookup"><span data-stu-id="a13d8-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a13d8-146">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="a13d8-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a13d8-147">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="a13d8-147">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> </dl>

 

 




