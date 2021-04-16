---
description: Essa é a propriedade de modo do objeto de sessão. Essa propriedade é um valor que representa o sinalizador de modo designado para a sessão de instalação atual. A maioria dos sinalizadores de modo são somente leitura externamente, mas alguns sinalizadores especificados também podem ser definidos.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Propriedade Session. Mode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757786"
---
# <a name="sessionmode-property"></a><span data-ttu-id="7b1b5-105">Propriedade Session. Mode</span><span class="sxs-lookup"><span data-stu-id="7b1b5-105">Session.Mode property</span></span>

<span data-ttu-id="7b1b5-106">Essa é a propriedade de **modo** do objeto de [**sessão**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="7b1b5-106">This is the **Mode** property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="7b1b5-107">Essa propriedade é um valor que representa o sinalizador de modo designado para a sessão de instalação atual.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-107">This property is a value representing the designated mode flag for the current install session.</span></span> <span data-ttu-id="7b1b5-108">A maioria dos sinalizadores de modo são somente leitura externamente, mas alguns sinalizadores especificados também podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-108">Most of the mode flags are read-only externally, but a few specified flags may be set as well.</span></span>

<span data-ttu-id="7b1b5-109">A função [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) retorna um booliano true ou false, indicando se a propriedade específica passada para a função está definida atualmente (true) ou não definida (false).</span><span class="sxs-lookup"><span data-stu-id="7b1b5-109">The [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function returns a Boolean TRUE or FALSE, indicating whether the specific property passed into the function is currently set (TRUE) or not set (FALSE).</span></span>

<span data-ttu-id="7b1b5-110">Observe que nem todos os valores do modo de execução do *sinalizador* estão disponíveis ao chamar a propriedade **Mode** de uma ação personalizada adiada.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-110">Note that not all the run mode values of *flag* are available when calling the **Mode** property from a deferred custom action.</span></span> <span data-ttu-id="7b1b5-111">Para obter mais informações, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="7b1b5-111">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="7b1b5-112">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b1b5-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b1b5-113">Syntax</span></span>


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a><span data-ttu-id="7b1b5-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7b1b5-114">Property value</span></span>

<span data-ttu-id="7b1b5-115">Valor inteiro necessário para o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-115">Required integer value for the flag.</span></span> <span data-ttu-id="7b1b5-116">Deve ser uma destas opções:</span><span class="sxs-lookup"><span data-stu-id="7b1b5-116">Must be one of the following:</span></span>



| <span data-ttu-id="7b1b5-117">Nome do sinalizador</span><span class="sxs-lookup"><span data-stu-id="7b1b5-117">Flag name</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="7b1b5-118">Significado</span><span class="sxs-lookup"><span data-stu-id="7b1b5-118">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <span data-ttu-id="7b1b5-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="7b1b5-120">Instalação do modo administrativo, caso contrário, instalação do produto.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-120">Administrative mode install, else product install.</span></span><br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <span data-ttu-id="7b1b5-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="7b1b5-122">Anúncio do modo de instalação.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-122">Advertise mode of install.</span></span><br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <span data-ttu-id="7b1b5-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="7b1b5-124">Banco de dados do modo de manutenção carregado.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-124">Maintenance mode database loaded.</span></span><br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <span data-ttu-id="7b1b5-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="7b1b5-126">A reversão está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-126">Rollback is enabled.</span></span><br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <span data-ttu-id="7b1b5-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="7b1b5-128">O arquivo de log está ativo.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-128">Log file is active.</span></span><br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <span data-ttu-id="7b1b5-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span></span> </dl>                          | <span data-ttu-id="7b1b5-130">Operações de execução ou de spool.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-130">Executing or spooling operations.</span></span><br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <span data-ttu-id="7b1b5-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span></span> </dl>                      | <span data-ttu-id="7b1b5-132">A reinicialização é necessária (configurável).</span><span class="sxs-lookup"><span data-stu-id="7b1b5-132">Reboot is needed (settable).</span></span><br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <span data-ttu-id="7b1b5-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span></span> </dl>                              | <span data-ttu-id="7b1b5-134">A reinicialização é necessária para continuar a instalação (configurável).</span><span class="sxs-lookup"><span data-stu-id="7b1b5-134">Reboot is needed to continue installation (settable).</span></span><br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <span data-ttu-id="7b1b5-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span></span> </dl>                                      | <span data-ttu-id="7b1b5-136">Instalando arquivos de gabinetes e arquivos usando a tabela de mídia.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-136">Installing files from cabinets and files using Media table.</span></span><br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <span data-ttu-id="7b1b5-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="7b1b5-138">Os arquivos de origem usam apenas nomes de arquivo curtos.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-138">Source files use only short file names.</span></span><br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <span data-ttu-id="7b1b5-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="7b1b5-140">Os arquivos de destino são apenas para usar nomes de arquivo curtos.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-140">Target files are to use only short file names.</span></span><br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <span data-ttu-id="7b1b5-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span></span> </dl>                             | <span data-ttu-id="7b1b5-142">O sistema operacional é o Windows 98/95.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-142">Operating system is Windows 98/95.</span></span><br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <span data-ttu-id="7b1b5-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span></span> </dl>                         | <span data-ttu-id="7b1b5-144">O sistema operacional dá suporte à publicidade de produtos.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-144">Operating system supports advertising of products.</span></span><br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <span data-ttu-id="7b1b5-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span></span> </dl>                             | <span data-ttu-id="7b1b5-146">[Ação personalizada](custom-actions.md) adiada chamada a partir da execução do script de instalação.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-146">Deferred [custom action](custom-actions.md) called from install script execution.</span></span><br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <span data-ttu-id="7b1b5-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="7b1b5-148">[Ação personalizada](custom-actions.md) adiada chamada do script de execução de reversão.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-148">Deferred [custom action](custom-actions.md) called from rollback execution script.</span></span><br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <span data-ttu-id="7b1b5-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="7b1b5-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span></span> </dl>                                         | <span data-ttu-id="7b1b5-150">[Ação personalizada](custom-actions.md) adiada chamada do script de execução de confirmação.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-150">Deferred [custom action](custom-actions.md) called from commit execution script.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="7b1b5-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b1b5-151">Requirements</span></span>



| <span data-ttu-id="7b1b5-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b1b5-152">Requirement</span></span> | <span data-ttu-id="7b1b5-153">Valor</span><span class="sxs-lookup"><span data-stu-id="7b1b5-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1b5-154">Versão</span><span class="sxs-lookup"><span data-stu-id="7b1b5-154">Version</span></span><br/> | <span data-ttu-id="7b1b5-155">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-155">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7b1b5-156">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7b1b5-156">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7b1b5-157">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b1b5-157">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



 

 




