---
description: Exclui um pacote de driver de impressora do repositório de drivers.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Função DeletePrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782466"
---
# <a name="deleteprinterdriverpackage-function"></a><span data-ttu-id="576c6-103">Função DeletePrinterDriverPackage</span><span class="sxs-lookup"><span data-stu-id="576c6-103">DeletePrinterDriverPackage function</span></span>

<span data-ttu-id="576c6-104">Exclui um pacote de driver de impressora do repositório de drivers.</span><span class="sxs-lookup"><span data-stu-id="576c6-104">Deletes a printer driver package from the driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="576c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="576c6-105">Syntax</span></span>


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a><span data-ttu-id="576c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="576c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="576c6-107">*pszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="576c6-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576c6-108">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão do qual o pacote de driver está sendo excluído.</span><span class="sxs-lookup"><span data-stu-id="576c6-108">A pointer to a constant, null-terminated string that specifies the name of the print server from which the driver package is being deleted.</span></span> <span data-ttu-id="576c6-109">Um valor de ponteiro **nulo** significa o computador local.</span><span class="sxs-lookup"><span data-stu-id="576c6-109">A **NULL** pointer value means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="576c6-110">*pszInfPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="576c6-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576c6-111">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o caminho para o \* arquivo. inf do driver.</span><span class="sxs-lookup"><span data-stu-id="576c6-111">A pointer to a constant, null-terminated string that specifies the path to the driver's \*.inf file.</span></span>

</dd> <dt>

<span data-ttu-id="576c6-112">*pszEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="576c6-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="576c6-113">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador (por exemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="576c6-113">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="576c6-114">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="576c6-114">This can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="576c6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="576c6-115">Return value</span></span>

<span data-ttu-id="576c6-116">S \_ OK, se a operação for concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="576c6-116">S\_OK, if the operation succeeds.</span></span>

<span data-ttu-id="576c6-117">E \_ ACCESSDENIED, se o pacote foi enviado com o Windows.</span><span class="sxs-lookup"><span data-stu-id="576c6-117">E\_ACCESSDENIED, if the package was shipped with Windows.</span></span>

<span data-ttu-id="576c6-118">\_Código HRESULT (erro \_ \_ \_ \_ de pacote de driver de impressão em \_ uso), se o pacote estiver sendo usado.</span><span class="sxs-lookup"><span data-stu-id="576c6-118">HRESULT\_CODE(ERROR\_PRINT\_DRIVER\_PACKAGE\_IN\_USE), if the package is being used.</span></span>

<span data-ttu-id="576c6-119">Caso contrário, o **HRESULT** conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="576c6-119">Otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="576c6-120">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="576c6-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="576c6-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="576c6-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="576c6-122">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="576c6-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="576c6-123">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="576c6-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="576c6-124">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="576c6-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="576c6-125">O repositório de drivers normalmente é% windir% \\ inf ou% windir% \\ System32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="576c6-125">The driver store is typically %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="576c6-126">Um pacote de driver fornecido com o Windows não pode ser removido com esta função.</span><span class="sxs-lookup"><span data-stu-id="576c6-126">A driver package that shipped with Windows cannot be removed with this function.</span></span>

<span data-ttu-id="576c6-127">O usuário deve ter privilégios de administração de impressora.</span><span class="sxs-lookup"><span data-stu-id="576c6-127">The user must have printer administration privileges.</span></span>

## <a name="requirements"></a><span data-ttu-id="576c6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="576c6-128">Requirements</span></span>



| <span data-ttu-id="576c6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="576c6-129">Requirement</span></span> | <span data-ttu-id="576c6-130">Valor</span><span class="sxs-lookup"><span data-stu-id="576c6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="576c6-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="576c6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="576c6-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="576c6-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="576c6-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="576c6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="576c6-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="576c6-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="576c6-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="576c6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="576c6-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="576c6-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="576c6-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="576c6-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="576c6-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="576c6-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="576c6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="576c6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="576c6-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="576c6-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="576c6-141">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="576c6-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="576c6-142">**DeletePrinterDriverPackageW** (Unicode) e **DeletePrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="576c6-142">**DeletePrinterDriverPackageW** (Unicode) and **DeletePrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="576c6-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="576c6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="576c6-144">Impressão</span><span class="sxs-lookup"><span data-stu-id="576c6-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="576c6-145">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="576c6-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

