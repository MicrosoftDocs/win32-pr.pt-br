---
description: A função GetSpoolFileHandle recupera um identificador para o arquivo de spool associado ao trabalho enviado no momento pelo aplicativo.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: Função GetSpoolFileHandle (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011732"
---
# <a name="getspoolfilehandle-function"></a><span data-ttu-id="23fd6-103">Função GetSpoolFileHandle</span><span class="sxs-lookup"><span data-stu-id="23fd6-103">GetSpoolFileHandle function</span></span>

<span data-ttu-id="23fd6-104">A função **GetSpoolFileHandle** recupera um identificador para o arquivo de spool associado ao trabalho enviado no momento pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="23fd6-104">The **GetSpoolFileHandle** function retrieves a handle for the spool file associated with the job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="23fd6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23fd6-105">Syntax</span></span>


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="23fd6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23fd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23fd6-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23fd6-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23fd6-108">Um identificador para a impressora para a qual o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="23fd6-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="23fd6-109">Deve ser o mesmo identificador que foi usado para enviar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="23fd6-109">This should be the same handle that was used to submit the job.</span></span> <span data-ttu-id="23fd6-110">(Use a função [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.)</span><span class="sxs-lookup"><span data-stu-id="23fd6-110">(Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23fd6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23fd6-111">Return value</span></span>

<span data-ttu-id="23fd6-112">Se a função for realizada com sucesso, ela retornará um identificador para o arquivo de spool.</span><span class="sxs-lookup"><span data-stu-id="23fd6-112">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="23fd6-113">Se a função falhar, ela retornará **um \_ \_ valor de identificador inválido**.</span><span class="sxs-lookup"><span data-stu-id="23fd6-113">If the function fails, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="23fd6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="23fd6-114">Remarks</span></span>

<span data-ttu-id="23fd6-115">Com o identificador para o arquivo de spool, seu aplicativo pode gravar no arquivo de spool com chamadas para [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) seguido por [**CommitSpoolData**](commitspooldata.md).</span><span class="sxs-lookup"><span data-stu-id="23fd6-115">With the handle to the spool file, your application can write to the spool file with calls to [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) followed by [**CommitSpoolData**](commitspooldata.md).</span></span>

<span data-ttu-id="23fd6-116">Seu aplicativo não deve chamar [**ClosePrinter**](closeprinter.md) em *hPrinter* até depois de ter acessado o arquivo de spool pela última vez.</span><span class="sxs-lookup"><span data-stu-id="23fd6-116">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="23fd6-117">Em seguida, ele deve chamar [**CloseSpoolFileHandle**](closespoolfilehandle.md) seguido por **ClosePrinter**.</span><span class="sxs-lookup"><span data-stu-id="23fd6-117">Then it should call [**CloseSpoolFileHandle**](closespoolfilehandle.md) followed by **ClosePrinter**.</span></span> <span data-ttu-id="23fd6-118">As tentativas de acessar o identificador de arquivo de spool depois que o *hPrinter* original foi fechado falharão mesmo que o próprio identificador de arquivo não tenha sido fechado.</span><span class="sxs-lookup"><span data-stu-id="23fd6-118">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="23fd6-119">O **CloseSpoolFileHandle** , por si só, falhará se **ClosePrinter** for chamado primeiro.</span><span class="sxs-lookup"><span data-stu-id="23fd6-119">**CloseSpoolFileHandle** will itself fail if **ClosePrinter** is called first.</span></span>

<span data-ttu-id="23fd6-120">Essa função falhará se for chamada antes que o trabalho de impressão tenha terminado o spool.</span><span class="sxs-lookup"><span data-stu-id="23fd6-120">This function will fail if it is called before the print job has finished spooling.</span></span>

## <a name="requirements"></a><span data-ttu-id="23fd6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23fd6-121">Requirements</span></span>



| <span data-ttu-id="23fd6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fd6-122">Requirement</span></span> | <span data-ttu-id="23fd6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="23fd6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23fd6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23fd6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="23fd6-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23fd6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="23fd6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23fd6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="23fd6-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23fd6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="23fd6-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23fd6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="23fd6-129"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23fd6-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="23fd6-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23fd6-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="23fd6-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23fd6-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="23fd6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="23fd6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23fd6-133"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="23fd6-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="23fd6-134">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="23fd6-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="23fd6-135">**GetSpoolFileHandleW** (Unicode) e **GetSpoolFileHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="23fd6-135">**GetSpoolFileHandleW** (Unicode) and **GetSpoolFileHandleA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="23fd6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="23fd6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23fd6-137">Impressão</span><span class="sxs-lookup"><span data-stu-id="23fd6-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="23fd6-138">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="23fd6-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="23fd6-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="23fd6-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="23fd6-140">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="23fd6-140">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="23fd6-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="23fd6-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="23fd6-142">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="23fd6-142">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="23fd6-143">**CommitSpoolData**</span><span class="sxs-lookup"><span data-stu-id="23fd6-143">**CommitSpoolData**</span></span>](commitspooldata.md)
</dt> </dl>

 

