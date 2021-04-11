---
description: Instala um driver de impressora de um pacote de driver que está no repositório de drivers de servidores de impressão.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Função InstallPrinterDriverFromPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171708"
---
# <a name="installprinterdriverfrompackage-function"></a><span data-ttu-id="85f66-103">Função InstallPrinterDriverFromPackage</span><span class="sxs-lookup"><span data-stu-id="85f66-103">InstallPrinterDriverFromPackage function</span></span>

<span data-ttu-id="85f66-104">Instala um driver de impressora de um pacote de driver que está no repositório de drivers do servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="85f66-104">Installs a printer driver from a driver package that is in the print server's driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85f66-105">Syntax</span></span>


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="85f66-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85f66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85f66-107">*pszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85f66-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f66-108">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="85f66-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="85f66-109">**NULL** significa o computador local.</span><span class="sxs-lookup"><span data-stu-id="85f66-109">**NULL** means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="85f66-110">*pszInfPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85f66-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f66-111">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o caminho do repositório de drivers para o arquivo. inf do driver de impressão.</span><span class="sxs-lookup"><span data-stu-id="85f66-111">A pointer to a constant, null-terminated string that specifies the driver store path to the print driver's .inf file.</span></span> <span data-ttu-id="85f66-112">**NULL** significa que o driver está em um arquivo inf fornecido com o Windows.</span><span class="sxs-lookup"><span data-stu-id="85f66-112">**NULL** means the driver is in an inf file that shipped with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="85f66-113">*pszDriverName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85f66-113">*pszDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f66-114">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do driver.</span><span class="sxs-lookup"><span data-stu-id="85f66-114">A pointer to a constant, null-terminated string that specifies the name of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="85f66-115">*pszEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85f66-115">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f66-116">Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador (por exemplo, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="85f66-116">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="85f66-117">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="85f66-117">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85f66-118">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="85f66-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85f66-119">Isso pode ser somente 0 ou IPDFP \_ copiar \_ todos os \_ arquivos.</span><span class="sxs-lookup"><span data-stu-id="85f66-119">This can only be 0 or IPDFP\_COPY\_ALL\_FILES.</span></span> <span data-ttu-id="85f66-120">Um valor de 0 significa que o driver de impressora deve ser adicionado e todos os arquivos no diretório de driver de impressora mais novos do que os arquivos correspondentes atualmente em uso devem ser copiados.</span><span class="sxs-lookup"><span data-stu-id="85f66-120">A value of 0 means that the printer driver must be added and any files in the printer driver directory that are newer than corresponding files currently in use must be copied.</span></span> <span data-ttu-id="85f66-121">Um valor de IPDFP \_ copiar \_ todos os \_ arquivos significa que o driver de impressora e todos os arquivos no diretório do driver de impressora devem ser adicionados.</span><span class="sxs-lookup"><span data-stu-id="85f66-121">A value of IPDFP\_COPY\_ALL\_FILES means the printer driver and all the files in the printer driver directory must be added.</span></span> <span data-ttu-id="85f66-122">Os carimbos de data/hora do arquivo são ignorados quando *dwFlags* tem um valor de IPDFP \_ copiar \_ todos os \_ arquivos.</span><span class="sxs-lookup"><span data-stu-id="85f66-122">The file time stamps are ignored when *dwFlags* has a value of IPDFP\_COPY\_ALL\_FILES.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85f66-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85f66-123">Return value</span></span>

<span data-ttu-id="85f66-124">Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="85f66-124">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="85f66-125">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="85f66-125">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="85f66-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="85f66-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="85f66-127">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="85f66-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="85f66-128">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="85f66-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="85f66-129">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="85f66-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="85f66-130">O repositório de drivers normalmente é% windir% \\ inf ou% windir% \\ System32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="85f66-130">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="85f66-131">O **InstallPrinterDriverFromPackage** também instala outros arquivos no pacote, como perfis de cor e processadores de impressão.</span><span class="sxs-lookup"><span data-stu-id="85f66-131">**InstallPrinterDriverFromPackage** also installs other files in the package, such as color profiles and print processors.</span></span>

<span data-ttu-id="85f66-132">Os usuários devem ter direitos de administração de impressora para serem instalados em um computador remoto ou no computador local quando o usuário estiver conectado com os serviços de terminal.</span><span class="sxs-lookup"><span data-stu-id="85f66-132">Users must have printer administration rights to install either on a remote computer or on the local computer when the user is logged in with Terminal Services.</span></span>

<span data-ttu-id="85f66-133">Somente pacotes assinados podem ser instalados em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="85f66-133">Only signed packages can be installed on a remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="85f66-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85f66-134">Requirements</span></span>



| <span data-ttu-id="85f66-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="85f66-135">Requirement</span></span> | <span data-ttu-id="85f66-136">Valor</span><span class="sxs-lookup"><span data-stu-id="85f66-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85f66-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85f66-137">Minimum supported client</span></span><br/> | <span data-ttu-id="85f66-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85f66-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="85f66-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85f66-139">Minimum supported server</span></span><br/> | <span data-ttu-id="85f66-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85f66-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="85f66-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85f66-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="85f66-142"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85f66-142"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="85f66-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85f66-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="85f66-144"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85f66-144"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="85f66-145">DLL</span><span class="sxs-lookup"><span data-stu-id="85f66-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85f66-146"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85f66-146"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="85f66-147">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="85f66-147">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="85f66-148">**InstallPrinterDriverFromPackageW** (Unicode) e **InstallPrinterDriverFromPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="85f66-148">**InstallPrinterDriverFromPackageW** (Unicode) and **InstallPrinterDriverFromPackageA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="85f66-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="85f66-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f66-150">Impressão</span><span class="sxs-lookup"><span data-stu-id="85f66-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="85f66-151">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="85f66-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

