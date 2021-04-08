---
description: A função CommitSpoolData notifica o spooler de impressão que uma quantidade especificada de dados foi gravada em um arquivo de spool especificado e está pronta para ser renderizada.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: Função CommitSpoolData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828210"
---
# <a name="commitspooldata-function"></a><span data-ttu-id="00c4a-103">Função CommitSpoolData</span><span class="sxs-lookup"><span data-stu-id="00c4a-103">CommitSpoolData function</span></span>

<span data-ttu-id="00c4a-104">A função **CommitSpoolData** notifica o spooler de impressão que uma quantidade especificada de dados foi gravada em um arquivo de spool especificado e está pronta para ser renderizada.</span><span class="sxs-lookup"><span data-stu-id="00c4a-104">The **CommitSpoolData** function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00c4a-105">Syntax</span></span>


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a><span data-ttu-id="00c4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00c4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c4a-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00c4a-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c4a-108">Um identificador para a impressora para a qual o trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="00c4a-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="00c4a-109">Deve ser o mesmo identificador que foi usado para obter *hSpoolFile* com [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="00c4a-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="00c4a-110">*hSpoolFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="00c4a-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c4a-111">Um identificador para o arquivo de spool que está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="00c4a-111">A handle to the spool file being changed.</span></span> <span data-ttu-id="00c4a-112">Na primeira chamada de **CommitSpoolData**, deve ser o mesmo identificador retornado por [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="00c4a-112">On the first call of **CommitSpoolData**, this should be the same handle that was returned by [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span> <span data-ttu-id="00c4a-113">As chamadas subsequentes para **CommitSpoolData** devem passar o identificador retornado pela chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="00c4a-113">Subsequent calls to **CommitSpoolData** should pass the handle returned by the preceding call.</span></span> <span data-ttu-id="00c4a-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="00c4a-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="00c4a-115">*cbCommit*</span><span class="sxs-lookup"><span data-stu-id="00c4a-115">*cbCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="00c4a-116">O número de bytes confirmados para o spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="00c4a-116">The number of bytes committed to the print spooler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c4a-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00c4a-117">Return value</span></span>

<span data-ttu-id="00c4a-118">Se a função for realizada com sucesso, ela retornará um identificador para o arquivo de spool.</span><span class="sxs-lookup"><span data-stu-id="00c4a-118">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="00c4a-119">Se a função falhar, ela retornará um \_ valor de identificador inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="00c4a-119">If the function fails, it returns INVALID\_HANDLE\_VALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="00c4a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="00c4a-120">Remarks</span></span>

<span data-ttu-id="00c4a-121">Os aplicativos que enviam um trabalho de impressão do spooler podem chamar [**GetSpoolFileHandle**](getspoolfilehandle.md) e, em seguida, gravar dados diretamente no identificador do arquivo de spool chamando [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span><span class="sxs-lookup"><span data-stu-id="00c4a-121">Applications submitting a spooler print job can call [**GetSpoolFileHandle**](getspoolfilehandle.md) and then directly write data to the spool file handle by calling [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span></span> <span data-ttu-id="00c4a-122">Para notificar o spooler de impressão de que o arquivo contém dados que estão prontos para serem renderizados, o aplicativo deve chamar **CommitSpoolData** e fornecer o número de bytes disponíveis.</span><span class="sxs-lookup"><span data-stu-id="00c4a-122">To notify the print spooler that the file contains data which is ready to be rendered, the application must call **CommitSpoolData** and provide the number of available bytes.</span></span>

<span data-ttu-id="00c4a-123">Se **CommitSpoolData** for chamado várias vezes, cada chamada deverá usar o identificador de arquivo de spool retornado pela chamada anterior.</span><span class="sxs-lookup"><span data-stu-id="00c4a-123">If **CommitSpoolData** is called multiple times, each call must use the spool file handle returned by the previous call.</span></span> <span data-ttu-id="00c4a-124">Quando não forem gravados mais dados no arquivo de spool, [**CloseSpoolFileHandle**](closespoolfilehandle.md) deverá ser chamado para o identificador de arquivo retornado pela última chamada para **CommitSpoolData**.</span><span class="sxs-lookup"><span data-stu-id="00c4a-124">When no more data will be written to the spool file, [**CloseSpoolFileHandle**](closespoolfilehandle.md) should be called for the file handle returned by the last call to **CommitSpoolData**.</span></span>

<span data-ttu-id="00c4a-125">Antes de chamar **CommitSpoolData**, os aplicativos devem definir o ponteiro do arquivo para a posição que ele tinha antes de gravar dados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="00c4a-125">Before calling **CommitSpoolData**, applications must set the file pointer to the position it had before it wrote data to the file.</span></span> <span data-ttu-id="00c4a-126">No processo de renderização dos dados no arquivo de spooler, o spooler de impressão moverá o ponteiro do arquivo de spool *cbCommit* bytes do valor atual do ponteiro do arquivo.</span><span class="sxs-lookup"><span data-stu-id="00c4a-126">In the process of rendering the data in the spooler file, the print spooler will move the spool file pointer *cbCommit* bytes from the current value of file pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="00c4a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00c4a-127">Requirements</span></span>



| <span data-ttu-id="00c4a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="00c4a-128">Requirement</span></span> | <span data-ttu-id="00c4a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="00c4a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00c4a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00c4a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="00c4a-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00c4a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="00c4a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00c4a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="00c4a-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="00c4a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="00c4a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00c4a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="00c4a-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00c4a-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="00c4a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00c4a-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="00c4a-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00c4a-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="00c4a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="00c4a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00c4a-139"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="00c4a-139"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="00c4a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="00c4a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c4a-141">Impressão</span><span class="sxs-lookup"><span data-stu-id="00c4a-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="00c4a-142">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="00c4a-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="00c4a-143">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="00c4a-143">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="00c4a-144">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="00c4a-144">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> </dl>

 

