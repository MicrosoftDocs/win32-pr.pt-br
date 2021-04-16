---
description: O método EnableLog do objeto instalador habilita o registro em log do tipo de mensagem selecionado para todas as sessões de instalação subsequentes no espaço de processo atual.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Método Installer. EnableLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750000"
---
# <a name="installerenablelog-method"></a><span data-ttu-id="05de6-103">Método Installer. EnableLog</span><span class="sxs-lookup"><span data-stu-id="05de6-103">Installer.EnableLog method</span></span>

<span data-ttu-id="05de6-104">O método **EnableLog** do objeto [**instalador**](installer-object.md) habilita o registro em log do tipo de mensagem selecionado para todas as sessões de instalação subsequentes no espaço de processo atual.</span><span class="sxs-lookup"><span data-stu-id="05de6-104">The **EnableLog** method of the [**Installer**](installer-object.md) object enables logging of the selected message type for all subsequent installation sessions in the current process space.</span></span>

## <a name="syntax"></a><span data-ttu-id="05de6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="05de6-105">Syntax</span></span>


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a><span data-ttu-id="05de6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05de6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05de6-107">*logMode*</span><span class="sxs-lookup"><span data-stu-id="05de6-107">*logMode*</span></span> 
</dt> <dd>

<span data-ttu-id="05de6-108">Uma cadeia de caracteres necessária que contém letras que representam os tipos de mensagem a serem registradas.</span><span class="sxs-lookup"><span data-stu-id="05de6-108">A required string that contains letters representing the message types to log.</span></span> <span data-ttu-id="05de6-109">A cadeia de caracteres pode ser uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="05de6-109">The string can be a combination of the following values.</span></span>



| <span data-ttu-id="05de6-110">Valor</span><span class="sxs-lookup"><span data-stu-id="05de6-110">Value</span></span> | <span data-ttu-id="05de6-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="05de6-111">Description</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05de6-112">I</span><span class="sxs-lookup"><span data-stu-id="05de6-112">I</span></span>     | <span data-ttu-id="05de6-113">Mensagens somente de informações.</span><span class="sxs-lookup"><span data-stu-id="05de6-113">Information-only messages.</span></span>                                                                             |
| <span data-ttu-id="05de6-114">w</span><span class="sxs-lookup"><span data-stu-id="05de6-114">w</span></span>     | <span data-ttu-id="05de6-115">Mensagens de aviso não fatais.</span><span class="sxs-lookup"><span data-stu-id="05de6-115">Non-fatal warning messages.</span></span>                                                                            |
| <span data-ttu-id="05de6-116">e</span><span class="sxs-lookup"><span data-stu-id="05de6-116">e</span></span>     | <span data-ttu-id="05de6-117">Mensagens de erro que podem ser erros fatais.</span><span class="sxs-lookup"><span data-stu-id="05de6-117">Error messages that may be fatal errors.</span></span>                                                               |
| <span data-ttu-id="05de6-118">f</span><span class="sxs-lookup"><span data-stu-id="05de6-118">f</span></span>     | <span data-ttu-id="05de6-119">Lista de arquivos em uso que precisam ser substituídos.</span><span class="sxs-lookup"><span data-stu-id="05de6-119">List of files in use that need to be replaced.</span></span>                                                         |
| <span data-ttu-id="05de6-120">um</span><span class="sxs-lookup"><span data-stu-id="05de6-120">a</span></span>     | <span data-ttu-id="05de6-121">Início da notificação de ação.</span><span class="sxs-lookup"><span data-stu-id="05de6-121">Start of action notification.</span></span>                                                                          |
| <span data-ttu-id="05de6-122">r</span><span class="sxs-lookup"><span data-stu-id="05de6-122">r</span></span>     | <span data-ttu-id="05de6-123">Registro de dados de ação contendo conteúdo específico à ação.</span><span class="sxs-lookup"><span data-stu-id="05de6-123">Action data record containing content specific to action.</span></span>                                              |
| <span data-ttu-id="05de6-124">u</span><span class="sxs-lookup"><span data-stu-id="05de6-124">u</span></span>     | <span data-ttu-id="05de6-125">Mensagens de solicitação do usuário.</span><span class="sxs-lookup"><span data-stu-id="05de6-125">User request messages.</span></span>                                                                                 |
| <span data-ttu-id="05de6-126">c</span><span class="sxs-lookup"><span data-stu-id="05de6-126">c</span></span>     | <span data-ttu-id="05de6-127">Parâmetros de inicialização da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="05de6-127">UI initialization parameters.</span></span>                                                                          |
| <span data-ttu-id="05de6-128">m</span><span class="sxs-lookup"><span data-stu-id="05de6-128">m</span></span>     | <span data-ttu-id="05de6-129">Mensagem de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="05de6-129">Out-of-memory message.</span></span>                                                                                 |
| <span data-ttu-id="05de6-130">v</span><span class="sxs-lookup"><span data-stu-id="05de6-130">v</span></span>     | <span data-ttu-id="05de6-131">O envia grandes quantidades de informações para o arquivo de log, o que geralmente não é útil para os usuários.</span><span class="sxs-lookup"><span data-stu-id="05de6-131">Sends large amounts of information to log file not generally useful to users.</span></span> <span data-ttu-id="05de6-132">Pode ser usado para suporte.</span><span class="sxs-lookup"><span data-stu-id="05de6-132">May be used for support.</span></span> |
| <span data-ttu-id="05de6-133">p</span><span class="sxs-lookup"><span data-stu-id="05de6-133">p</span></span>     | <span data-ttu-id="05de6-134">Despejar tabela de propriedades; "Property = Value" na terminação do mecanismo</span><span class="sxs-lookup"><span data-stu-id="05de6-134">Dump property table; "property = value" at engine termination</span></span>                                          |
| \+    | <span data-ttu-id="05de6-135">Anexar ao arquivo de log existente.</span><span class="sxs-lookup"><span data-stu-id="05de6-135">Append to existing log file.</span></span>                                                                           |
| <span data-ttu-id="05de6-136">!</span><span class="sxs-lookup"><span data-stu-id="05de6-136">!</span></span>     | <span data-ttu-id="05de6-137">Libere cada linha para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="05de6-137">Flush each line to the log file.</span></span>                                                                       |
| <span data-ttu-id="05de6-138">x</span><span class="sxs-lookup"><span data-stu-id="05de6-138">x</span></span>     | <span data-ttu-id="05de6-139">Informações adicionais de depuração.</span><span class="sxs-lookup"><span data-stu-id="05de6-139">Extra debugging information.</span></span> <span data-ttu-id="05de6-140">Essa opção só está disponível com o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="05de6-140">This option only available with Windows Server 2003.</span></span>                      |
| <span data-ttu-id="05de6-141">o</span><span class="sxs-lookup"><span data-stu-id="05de6-141">o</span></span>     | <span data-ttu-id="05de6-142">Mensagens de espaço em disco insuficientes.</span><span class="sxs-lookup"><span data-stu-id="05de6-142">Out-of-disk-space messages.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="05de6-143">*Restaura*</span><span class="sxs-lookup"><span data-stu-id="05de6-143">*logFile*</span></span> 
</dt> <dd>

<span data-ttu-id="05de6-144">Cadeia de caracteres necessária que contém o caminho para o arquivo de log a ser criado.</span><span class="sxs-lookup"><span data-stu-id="05de6-144">Required string containing the path to the log file to be created.</span></span> <span data-ttu-id="05de6-145">Use uma cadeia de caracteres vazia ("") para desativar o registro em log.</span><span class="sxs-lookup"><span data-stu-id="05de6-145">Use an empty string ("") to turn off logging.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05de6-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05de6-146">Return value</span></span>

<span data-ttu-id="05de6-147">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="05de6-147">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05de6-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="05de6-148">Remarks</span></span>

<span data-ttu-id="05de6-149">O caminho para o local do arquivo de log já deve existir ao usar esse método.</span><span class="sxs-lookup"><span data-stu-id="05de6-149">The path to the logfile location must already exist when using this method.</span></span> <span data-ttu-id="05de6-150">O instalador não cria a estrutura de diretório para o arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="05de6-150">The Installer does not create the directory structure for the logfile.</span></span>

<span data-ttu-id="05de6-151">As opções de log definidas usando **EnableLog** substituem as configurações de política de registro em log existentes do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="05de6-151">The logging options set using **EnableLog** override any existing Windows Installer logging policy settings.</span></span>

<span data-ttu-id="05de6-152">O registro em log substitui um arquivo de log existente por padrão.</span><span class="sxs-lookup"><span data-stu-id="05de6-152">Logging overwrites an existing log file by default.</span></span> <span data-ttu-id="05de6-153">Você deve usar a letra ' + ' no modo de log para acrescentar a um arquivo de log existente.</span><span class="sxs-lookup"><span data-stu-id="05de6-153">You must use the '+' letter in the logging mode to append to an existing log file.</span></span>

<span data-ttu-id="05de6-154">A opção '! ' não é recomendada porque pode ter uma instalação significativamente lenta.</span><span class="sxs-lookup"><span data-stu-id="05de6-154">The '!' option is not recommended because it can significantly slow installation.</span></span> <span data-ttu-id="05de6-155">Essa opção pode ser útil ao depurar uma instalação.</span><span class="sxs-lookup"><span data-stu-id="05de6-155">This option may be useful when debugging an installation.</span></span>

<span data-ttu-id="05de6-156">O script de exemplo a seguir ativa o log detalhado para uma instalação.</span><span class="sxs-lookup"><span data-stu-id="05de6-156">The following sample script turns on verbose logging for an installation.</span></span> <span data-ttu-id="05de6-157">No final da instalação, o arquivo de log gerado estará em c: \\ temp \\ install. log.</span><span class="sxs-lookup"><span data-stu-id="05de6-157">At the end of the installation, the generated log file will be at c:\\temp\\install.log.</span></span>


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a><span data-ttu-id="05de6-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05de6-158">Requirements</span></span>



| <span data-ttu-id="05de6-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="05de6-159">Requirement</span></span> | <span data-ttu-id="05de6-160">Valor</span><span class="sxs-lookup"><span data-stu-id="05de6-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05de6-161">Versão</span><span class="sxs-lookup"><span data-stu-id="05de6-161">Version</span></span><br/> | <span data-ttu-id="05de6-162">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05de6-162">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="05de6-163">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="05de6-163">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="05de6-164">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="05de6-164">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="05de6-165">DLL</span><span class="sxs-lookup"><span data-stu-id="05de6-165">DLL</span></span><br/>     | <dl> <span data-ttu-id="05de6-166"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05de6-166"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="05de6-167">IID</span><span class="sxs-lookup"><span data-stu-id="05de6-167">IID</span></span><br/>     | <span data-ttu-id="05de6-168">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="05de6-168">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="05de6-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="05de6-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05de6-170">Log de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="05de6-170">Windows Installer Logging</span></span>](windows-installer-logging.md)
</dt> </dl>

 

 




