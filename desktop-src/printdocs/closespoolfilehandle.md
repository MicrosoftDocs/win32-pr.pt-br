---
description: A função CloseSpoolFileHandle fecha um identificador para um arquivo de spool associado ao trabalho de impressão atualmente enviado pelo aplicativo.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: Função CloseSpoolFileHandle (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758497"
---
# <a name="closespoolfilehandle-function"></a><span data-ttu-id="85759-103">Função CloseSpoolFileHandle</span><span class="sxs-lookup"><span data-stu-id="85759-103">CloseSpoolFileHandle function</span></span>

<span data-ttu-id="85759-104">A função **CloseSpoolFileHandle** fecha um identificador para um arquivo de spool associado ao trabalho de impressão atualmente enviado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85759-104">The **CloseSpoolFileHandle** function closes a handle to a spool file associated with the print job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="85759-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85759-105">Syntax</span></span>


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a><span data-ttu-id="85759-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85759-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85759-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85759-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85759-108">Um identificador para a impressora para a qual o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="85759-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="85759-109">Deve ser o mesmo identificador que foi usado para obter *hSpoolFile* com [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="85759-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="85759-110">*hSpoolFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85759-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85759-111">Um identificador para o arquivo de spool que está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="85759-111">A handle to the spool file being closed.</span></span> <span data-ttu-id="85759-112">Se [**CommitSpoolData**](commitspooldata.md) não tiver sido chamado desde que [**GetSpoolFileHandle**](getspoolfilehandle.md) foi chamado, ele deverá ser o mesmo identificador retornado por **GetSpoolFileHandle**.</span><span class="sxs-lookup"><span data-stu-id="85759-112">If [**CommitSpoolData**](commitspooldata.md) has not been called since [**GetSpoolFileHandle**](getspoolfilehandle.md) was called, then this should be the same handle that was returned by **GetSpoolFileHandle**.</span></span> <span data-ttu-id="85759-113">Caso contrário, ele deve ser o identificador que foi retornado pela chamada mais recente para **CommitSpoolData**.</span><span class="sxs-lookup"><span data-stu-id="85759-113">Otherwise, it should be the handle that was returned by the most recent call to **CommitSpoolData**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85759-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85759-114">Return value</span></span>

<span data-ttu-id="85759-115">**True**, se tiver sucesso; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="85759-115">**TRUE**, if it succeeds, **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="85759-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="85759-116">Remarks</span></span>

<span data-ttu-id="85759-117">Seu aplicativo não deve chamar [**ClosePrinter**](closeprinter.md) em *hPrinter* até depois de ter acessado o arquivo de spool pela última vez.</span><span class="sxs-lookup"><span data-stu-id="85759-117">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="85759-118">Em seguida, ele deve chamar **CloseSpoolFileHandle** seguido por **ClosePrinter**.</span><span class="sxs-lookup"><span data-stu-id="85759-118">Then it should call **CloseSpoolFileHandle** followed by **ClosePrinter**.</span></span> <span data-ttu-id="85759-119">As tentativas de acessar o identificador de arquivo de spool depois que o *hPrinter* original foi fechado falharão mesmo que o próprio identificador de arquivo não tenha sido fechado.</span><span class="sxs-lookup"><span data-stu-id="85759-119">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="85759-120">**CloseSpoolFileHandle** falhará se **ClosePrinter** for chamado primeiro.</span><span class="sxs-lookup"><span data-stu-id="85759-120">**CloseSpoolFileHandle** will fail if **ClosePrinter** is called first.</span></span>

## <a name="requirements"></a><span data-ttu-id="85759-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85759-121">Requirements</span></span>



| <span data-ttu-id="85759-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="85759-122">Requirement</span></span> | <span data-ttu-id="85759-123">Valor</span><span class="sxs-lookup"><span data-stu-id="85759-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85759-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85759-124">Minimum supported client</span></span><br/> | <span data-ttu-id="85759-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85759-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="85759-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85759-126">Minimum supported server</span></span><br/> | <span data-ttu-id="85759-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85759-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="85759-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85759-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="85759-129"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85759-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="85759-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85759-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="85759-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85759-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="85759-132">DLL</span><span class="sxs-lookup"><span data-stu-id="85759-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85759-133"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="85759-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="85759-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="85759-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85759-135">Impressão</span><span class="sxs-lookup"><span data-stu-id="85759-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="85759-136">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="85759-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="85759-137">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="85759-137">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="85759-138">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="85759-138">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> </dl>

 

 




