---
description: A propriedade MsiLogging define o modo de log padrão para o pacote de Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Propriedade MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782784"
---
# <a name="msilogging-property"></a><span data-ttu-id="47d51-103">Propriedade MsiLogging</span><span class="sxs-lookup"><span data-stu-id="47d51-103">MsiLogging property</span></span>

<span data-ttu-id="47d51-104">A propriedade **MsiLogging** define o modo de log padrão para o pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="47d51-104">The **MsiLogging** property sets the default logging mode for the Windows Installer package.</span></span> <span data-ttu-id="47d51-105">Se essa propriedade opcional estiver presente na [tabela de propriedades](property-table.md), o instalador gerará um arquivo de log chamado MSI \* . Façam.</span><span class="sxs-lookup"><span data-stu-id="47d51-105">If this optional property is present in the [Property table](property-table.md), the installer generates a log file named MSI\*.LOG.</span></span> <span data-ttu-id="47d51-106">O caminho completo para o arquivo de log é fornecido pelo valor da propriedade [**MsiLogFileLocation**](msilogfilelocation.md) .</span><span class="sxs-lookup"><span data-stu-id="47d51-106">The full path to the log file is given by the value of the [**MsiLogFileLocation**](msilogfilelocation.md) property.</span></span>

## <a name="value"></a><span data-ttu-id="47d51-107">Valor</span><span class="sxs-lookup"><span data-stu-id="47d51-107">Value</span></span>

<span data-ttu-id="47d51-108">O valor dessa propriedade deve ser uma cadeia de caracteres dos caracteres a seguir que especificam o modo de log padrão.</span><span class="sxs-lookup"><span data-stu-id="47d51-108">The value of this property should be a string of the following characters that specify the default logging mode.</span></span>



| <span data-ttu-id="47d51-109">Valor</span><span class="sxs-lookup"><span data-stu-id="47d51-109">Value</span></span>                                                                        | <span data-ttu-id="47d51-110">Significado</span><span class="sxs-lookup"><span data-stu-id="47d51-110">Meaning</span></span>                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47d51-111"><dt>I</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-111"><dt>I</dt></span></span> </dl> | <span data-ttu-id="47d51-112">Mensagens de status.</span><span class="sxs-lookup"><span data-stu-id="47d51-112">Status messages.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="47d51-113"><dt>w</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-113"><dt>w</dt></span></span> </dl> | <span data-ttu-id="47d51-114">Avisos não fatais.</span><span class="sxs-lookup"><span data-stu-id="47d51-114">Nonfatal warnings.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="47d51-115"><dt>Oriental</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-115"><dt>e</dt></span></span> </dl> | <span data-ttu-id="47d51-116">Todas as mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="47d51-116">All error messages.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="47d51-117"><dt>um</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-117"><dt>a</dt></span></span> </dl> | <span data-ttu-id="47d51-118">Inicialização de ações.</span><span class="sxs-lookup"><span data-stu-id="47d51-118">Start up of actions.</span></span><br/>                                                |
| <dl> <span data-ttu-id="47d51-119"><dt>r</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-119"><dt>r</dt></span></span> </dl> | <span data-ttu-id="47d51-120">Registros específicos da ação.</span><span class="sxs-lookup"><span data-stu-id="47d51-120">Action-specific records.</span></span><br/>                                            |
| <dl> <span data-ttu-id="47d51-121"><dt>u</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-121"><dt>u</dt></span></span> </dl> | <span data-ttu-id="47d51-122">Solicitações do usuário.</span><span class="sxs-lookup"><span data-stu-id="47d51-122">User requests.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="47d51-123"><dt>c</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-123"><dt>c</dt></span></span> </dl> | <span data-ttu-id="47d51-124">Parâmetros iniciais da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="47d51-124">Initial UI parameters.</span></span><br/>                                              |
| <dl> <span data-ttu-id="47d51-125"><dt>m</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-125"><dt>m</dt></span></span> </dl> | <span data-ttu-id="47d51-126">Informações de saída fatal ou de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="47d51-126">Out-of-memory or fatal exit information.</span></span><br/>                            |
| <dl> <span data-ttu-id="47d51-127"><dt>o</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-127"><dt>o</dt></span></span> </dl> | <span data-ttu-id="47d51-128">Mensagens de espaço em disco insuficientes.</span><span class="sxs-lookup"><span data-stu-id="47d51-128">Out-of-disk-space messages.</span></span><br/>                                         |
| <dl> <span data-ttu-id="47d51-129"><dt>DTI</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-129"><dt>p</dt></span></span> </dl> | <span data-ttu-id="47d51-130">Propriedades do terminal.</span><span class="sxs-lookup"><span data-stu-id="47d51-130">Terminal properties.</span></span><br/>                                                |
| <dl> <span data-ttu-id="47d51-131"><dt>l</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-131"><dt>v</dt></span></span> </dl> | <span data-ttu-id="47d51-132">Saída detalhada.</span><span class="sxs-lookup"><span data-stu-id="47d51-132">Verbose output.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="47d51-133"><dt>x</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-133"><dt>x</dt></span></span> </dl> | <span data-ttu-id="47d51-134">Informações adicionais de depuração.</span><span class="sxs-lookup"><span data-stu-id="47d51-134">Extra debugging information.</span></span> <span data-ttu-id="47d51-135">Disponível somente no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="47d51-135">Only available on Windows Server 2003.</span></span><br/> |
| <dl> <span data-ttu-id="47d51-136"><dt>!</dt></span><span class="sxs-lookup"><span data-stu-id="47d51-136"><dt>!</dt></span></span> </dl> | <span data-ttu-id="47d51-137">Libere cada linha para o log.</span><span class="sxs-lookup"><span data-stu-id="47d51-137">Flush each line to the log.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="47d51-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="47d51-138">Remarks</span></span>

<span data-ttu-id="47d51-139">Essa propriedade está disponível a partir do Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="47d51-139">This property is available starting with Windows Installer 4.0.</span></span>

<span data-ttu-id="47d51-140">Você não pode usar os valores "+" e " \* " da opção/l no valor da propriedade **MsiLogging** .</span><span class="sxs-lookup"><span data-stu-id="47d51-140">You cannot use the "+" and "\*" values of the /L option in the value of the **MsiLogging** property.</span></span>

<span data-ttu-id="47d51-141">O modo de log pode ser definido usando a política, uma opção de linha de comando ou programaticamente.</span><span class="sxs-lookup"><span data-stu-id="47d51-141">The logging mode can be set using policy, a command-line option, or programmatically.</span></span> <span data-ttu-id="47d51-142">Isso substitui o modo de log padrão.</span><span class="sxs-lookup"><span data-stu-id="47d51-142">This overrides the default logging mode.</span></span> <span data-ttu-id="47d51-143">Para obter mais informações sobre todos os métodos que estão disponíveis para definir o modo de log, consulte [log normal](normal-logging.md) na seção [log de Windows Installer](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="47d51-143">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="47d51-144">Se a propriedade **MsiLogging** estiver presente na [tabela de propriedades](property-table.md), o modo de log padrão do pacote poderá ser modificado alterando o valor dessa propriedade usando uma transformação de banco de [dados](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="47d51-144">If the **MsiLogging** property is present in the [Property table](property-table.md), the default logging mode of the package can be modified by changing the value of this property using a [database transform](database-transforms.md).</span></span> <span data-ttu-id="47d51-145">O modo de log padrão não pode ser alterado usando um [pacote de patch](patch-packages.md) (um arquivo. msp).</span><span class="sxs-lookup"><span data-stu-id="47d51-145">The default logging mode cannot be changed using a [Patch Package](patch-packages.md) (a .msp file.)</span></span>

<span data-ttu-id="47d51-146">Se a propriedade **MsiLogging** tiver sido definida na [tabela de propriedades](property-table.md), o modo de log padrão para todos os usuários do computador poderá ser especificado definindo a política [DisableLoggingFromPackage](disableloggingfrompackage.md) e a política de registro em [log](logging.md) .</span><span class="sxs-lookup"><span data-stu-id="47d51-146">If the **MsiLogging** property has been set in the [Property table](property-table.md), the default logging mode for all users of the computer can be specified by setting both the [DisableLoggingFromPackage](disableloggingfrompackage.md) policy and [Logging](logging.md) policy.</span></span> <span data-ttu-id="47d51-147">A configuração da política DisableLoggingFromPackage e da política de log substituirá a propriedade **MsiLogging** para todos os pacotes.</span><span class="sxs-lookup"><span data-stu-id="47d51-147">Setting both the DisableLoggingFromPackage policy and Logging policy will override the **MsiLogging** property for all packages.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d51-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47d51-148">Requirements</span></span>



| <span data-ttu-id="47d51-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="47d51-149">Requirement</span></span> | <span data-ttu-id="47d51-150">Valor</span><span class="sxs-lookup"><span data-stu-id="47d51-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47d51-151">Versão</span><span class="sxs-lookup"><span data-stu-id="47d51-151">Version</span></span><br/> | <span data-ttu-id="47d51-152">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="47d51-152">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="47d51-153">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="47d51-153">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="47d51-154">Windows Installer 4,5 no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47d51-154">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="47d51-155">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="47d51-155">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47d51-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="47d51-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d51-157">Propriedades</span><span class="sxs-lookup"><span data-stu-id="47d51-157">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="47d51-158">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="47d51-158">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




