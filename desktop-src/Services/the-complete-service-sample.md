---
description: 'Saiba mais sobre: o exemplo de serviço completo'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: O exemplo de serviço completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754494"
---
# <a name="the-complete-service-sample"></a><span data-ttu-id="74e27-103">O exemplo de serviço completo</span><span class="sxs-lookup"><span data-stu-id="74e27-103">The Complete Service Sample</span></span>

<span data-ttu-id="74e27-104">Os tópicos nesta seção formam um exemplo de serviço completo:</span><span class="sxs-lookup"><span data-stu-id="74e27-104">The topics in this section form a complete service sample:</span></span>

-   <span data-ttu-id="74e27-105">[Sample.MC](sample-mc.md) (contém mensagens de erro)</span><span class="sxs-lookup"><span data-stu-id="74e27-105">[Sample.mc](sample-mc.md) (contains error messages)</span></span>
-   <span data-ttu-id="74e27-106">[Svc. cpp](svc-cpp.md) (contém o código de serviço)</span><span class="sxs-lookup"><span data-stu-id="74e27-106">[Svc.cpp](svc-cpp.md) (contains the service code)</span></span>
-   <span data-ttu-id="74e27-107">[SvcConfig. cpp](svcconfig-cpp.md) (contém o código de configuração de serviço)</span><span class="sxs-lookup"><span data-stu-id="74e27-107">[SvcConfig.cpp](svcconfig-cpp.md) (contains service configuration code)</span></span>
-   <span data-ttu-id="74e27-108">[SvcControl. cpp](svccontrol-cpp.md) (contém código de controle de serviço)</span><span class="sxs-lookup"><span data-stu-id="74e27-108">[SvcControl.cpp](svccontrol-cpp.md) (contains service control code)</span></span>

## <a name="building-the-service"></a><span data-ttu-id="74e27-109">Criando o serviço</span><span class="sxs-lookup"><span data-stu-id="74e27-109">Building the Service</span></span>

<span data-ttu-id="74e27-110">O procedimento a seguir descreve como criar o serviço e registrar a DLL de mensagem de evento.</span><span class="sxs-lookup"><span data-stu-id="74e27-110">The following procedure describes how to build the service and register the event message DLL.</span></span>

<span data-ttu-id="74e27-111">**Para compilar o serviço e registrar a DLL de mensagem de evento**</span><span class="sxs-lookup"><span data-stu-id="74e27-111">**To build the service and register the event message DLL**</span></span>

1.  <span data-ttu-id="74e27-112">Crie a DLL de mensagem do Sample.mc usando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="74e27-112">Build the message DLL from Sample.mc using the following steps:</span></span>
    1.  <span data-ttu-id="74e27-113">**MC-U sample.mc**</span><span class="sxs-lookup"><span data-stu-id="74e27-113">**mc -U sample.mc**</span></span>
    2.  <span data-ttu-id="74e27-114">**RC-r Sample. rc**</span><span class="sxs-lookup"><span data-stu-id="74e27-114">**rc -r sample.rc**</span></span>
    3.  <span data-ttu-id="74e27-115">**link-dll-NOENTRY -out:sample.dll amostra. res**</span><span class="sxs-lookup"><span data-stu-id="74e27-115">**link -dll -noentry -out:sample.dll sample.res**</span></span>
2.  <span data-ttu-id="74e27-116">Crie Svc.exe, SvcConfig.exe e SvcControl.exe de svc. cpp, SvcConfig. cpp e SvcControl. cpp, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="74e27-116">Build Svc.exe, SvcConfig.exe, and SvcControl.exe from Svc.cpp, SvcConfig.cpp, and SvcControl.cpp, respectively.</span></span>
3.  <span data-ttu-id="74e27-117">Crie a chave do registro **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application \\ SvcName** e adicione os seguintes valores de registro a essa chave.</span><span class="sxs-lookup"><span data-stu-id="74e27-117">Create the registry key **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\EventLog\\Application\\SvcName** and add the following registry values to this key.</span></span>

    | <span data-ttu-id="74e27-118">Valor</span><span class="sxs-lookup"><span data-stu-id="74e27-118">Value</span></span>                              | <span data-ttu-id="74e27-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="74e27-119">Type</span></span>       | <span data-ttu-id="74e27-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="74e27-120">Description</span></span>                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="74e27-121">**EventMessageFile**  =  *\_ caminho da dll*</span><span class="sxs-lookup"><span data-stu-id="74e27-121">**EventMessageFile** = *dll\_path*</span></span> | <span data-ttu-id="74e27-122">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="74e27-122">REG\_SZ</span></span>    | <span data-ttu-id="74e27-123">O caminho para a DLL somente de recursos que contém cadeias de caracteres que o serviço pode gravar no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="74e27-123">The path to the resource-only DLL that contains strings that the service can write to the event log.</span></span>               |
    | <span data-ttu-id="74e27-124">**TypesSupported** = 0x00000007</span><span class="sxs-lookup"><span data-stu-id="74e27-124">**TypesSupported** = 0x00000007</span></span>    | <span data-ttu-id="74e27-125">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="74e27-125">REG\_DWORD</span></span> | <span data-ttu-id="74e27-126">Uma máscara de bits que especifica os tipos de eventos com suporte.</span><span class="sxs-lookup"><span data-stu-id="74e27-126">A bit mask that specifies the supported event types.</span></span> <span data-ttu-id="74e27-127">O valor 0x000000007 indica que todos os tipos têm suporte.</span><span class="sxs-lookup"><span data-stu-id="74e27-127">The value 0x000000007 indicates that all types are supported.</span></span> |

    

     

## <a name="testing-the-service"></a><span data-ttu-id="74e27-128">Testando o serviço</span><span class="sxs-lookup"><span data-stu-id="74e27-128">Testing the Service</span></span>

<span data-ttu-id="74e27-129">O procedimento a seguir descreve como testar o serviço do.</span><span class="sxs-lookup"><span data-stu-id="74e27-129">The following procedure describes how to test the service.</span></span>

<span data-ttu-id="74e27-130">**Para testar o serviço**</span><span class="sxs-lookup"><span data-stu-id="74e27-130">**To test the service**</span></span>

1.  <span data-ttu-id="74e27-131">No painel de controle, inicie o aplicativo **Serviços** .</span><span class="sxs-lookup"><span data-stu-id="74e27-131">In Control Panel, start the **Services** application.</span></span> <span data-ttu-id="74e27-132">(Nas etapas a seguir, use a tecla F5 para atualizar a exibição depois de executar um comando que modifica as informações no aplicativo de **Serviços** .)</span><span class="sxs-lookup"><span data-stu-id="74e27-132">(In the following steps, use the F5 key to refresh the display after executing a command that modifies the information in the **Services** application.)</span></span>
2.  <span data-ttu-id="74e27-133">Execute o seguinte comando para instalar o serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-133">Run the following command to install the service:</span></span>

    <span data-ttu-id="74e27-134">**instalação do SVC**</span><span class="sxs-lookup"><span data-stu-id="74e27-134">**svc install**</span></span>

    <span data-ttu-id="74e27-135">O serviço grava "serviço instalado com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="74e27-135">The service writes "Service installed successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="74e27-136">Se a instalação do serviço for realizada com sucesso, o serviço será exibido no aplicativo **Serviços** .</span><span class="sxs-lookup"><span data-stu-id="74e27-136">If the service installation succeeds, the service is displayed in the **Services** application.</span></span> <span data-ttu-id="74e27-137">Observe que **Name** está definido como "SvcName", a **Descrição** e o **status** estão em branco e o **tipo de inicialização** é definido como "manual".</span><span class="sxs-lookup"><span data-stu-id="74e27-137">Note that **Name** is set to "SvcName", **Description** and **Status** are blank, and **Startup Type** is set to "Manual".</span></span>

3.  <span data-ttu-id="74e27-138">Execute o seguinte comando para iniciar o serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-138">Run the following command to start the service:</span></span>

    <span data-ttu-id="74e27-139">**svccontrol iniciar SvcName**</span><span class="sxs-lookup"><span data-stu-id="74e27-139">**svccontrol start SvcName**</span></span>

    <span data-ttu-id="74e27-140">Se a operação for concluída com sucesso, o programa de controle de serviço gravará "início do serviço pendente..." e "o serviço foi iniciado com êxito" no console do.</span><span class="sxs-lookup"><span data-stu-id="74e27-140">If the operation succeeds, the service control program writes "Service start pending..." and then "Service started successfully" to the console.</span></span> <span data-ttu-id="74e27-141">Caso contrário, o programa gravará uma mensagem de erro no console.</span><span class="sxs-lookup"><span data-stu-id="74e27-141">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="74e27-142">Se o serviço for iniciado com êxito, o **status** será definido como "iniciado".</span><span class="sxs-lookup"><span data-stu-id="74e27-142">If the service starts successfully, **Status** is set to "Started".</span></span> <span data-ttu-id="74e27-143">O código na função de [*immain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) é executado pelo SCM.</span><span class="sxs-lookup"><span data-stu-id="74e27-143">The code in the [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function is executed by the SCM.</span></span> <span data-ttu-id="74e27-144">Se ocorrer um erro, o serviço gravará uma mensagem de erro no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="74e27-144">If an error occurs, the service will write an error message to the event log.</span></span> <span data-ttu-id="74e27-145">Essa mensagem inclui o nome da função que falhou e o código de erro que foi retornado em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="74e27-145">This message includes the name of the function that failed and the error code that was returned on failure.</span></span>

4.  <span data-ttu-id="74e27-146">Execute o seguinte comando para atualizar a descrição do serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-146">Run the following command to update the service description:</span></span>

    <span data-ttu-id="74e27-147">**svcconfig descrever SvcName**</span><span class="sxs-lookup"><span data-stu-id="74e27-147">**svcconfig describe SvcName**</span></span>

    <span data-ttu-id="74e27-148">O programa de configuração de serviço grava "Descrição do serviço atualizada com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="74e27-148">The service configuration program writes "Service description updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="74e27-149">Se a atualização for realizada com sucesso, a **Descrição** será definida como "esta é uma descrição de teste".</span><span class="sxs-lookup"><span data-stu-id="74e27-149">If the update succeeds, **Description** is set to "This is a test description".</span></span>

5.  <span data-ttu-id="74e27-150">Execute o seguinte comando para consultar a configuração do serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-150">Run the following command to query the service configuration:</span></span>

    <span data-ttu-id="74e27-151">**svcconfig consulta SvcName**</span><span class="sxs-lookup"><span data-stu-id="74e27-151">**svcconfig query SvcName**</span></span>

    <span data-ttu-id="74e27-152">O programa de configuração de serviço grava as informações de configuração do serviço no console do se a operação for concluída com sucesso ou uma mensagem de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="74e27-152">The service configuration program writes the service configuration information to the console if the operation succeeds or an error message otherwise.</span></span>

6.  <span data-ttu-id="74e27-153">Execute o seguinte comando para alterar a DACL do serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-153">Run the following command to change the service DACL:</span></span>

    <span data-ttu-id="74e27-154">**svccontrol DACL SvcName**</span><span class="sxs-lookup"><span data-stu-id="74e27-154">**svccontrol dacl SvcName**</span></span>

    <span data-ttu-id="74e27-155">O programa de configuração de serviço grava o "serviço DACL atualizado com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="74e27-155">The service configuration program writes "Service DACL updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

7.  <span data-ttu-id="74e27-156">Execute o seguinte comando para desabilitar o serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-156">Run the following command to disable the service:</span></span>

    <span data-ttu-id="74e27-157">**svcconfig desabilitar SvcName**</span><span class="sxs-lookup"><span data-stu-id="74e27-157">**svcconfig disable SvcName**</span></span>

    <span data-ttu-id="74e27-158">O programa de configuração de serviço grava "serviço desabilitado com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro caso contrário.</span><span class="sxs-lookup"><span data-stu-id="74e27-158">The service configuration program writes "Service disabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="74e27-159">Se o serviço for desabilitado com êxito, o **tipo de inicialização** será definido como "desabilitado".</span><span class="sxs-lookup"><span data-stu-id="74e27-159">If the service is disabled successfully, **Startup Type** is set to "Disabled".</span></span>

8.  <span data-ttu-id="74e27-160">Execute o seguinte comando para habilitar o serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-160">Run the following command to enable the service:</span></span>

    <span data-ttu-id="74e27-161">**svcconfig habilitar SvcName**</span><span class="sxs-lookup"><span data-stu-id="74e27-161">**svcconfig enable SvcName**</span></span>

    <span data-ttu-id="74e27-162">O programa de configuração de serviço grava "serviço habilitado com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="74e27-162">The service configuration program writes "Service enabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="74e27-163">Se o serviço for habilitado com êxito, o **tipo de inicialização** será definido como "manual".</span><span class="sxs-lookup"><span data-stu-id="74e27-163">If the service is enabled successfully, **Startup Type** is set to "Manual".</span></span>

9.  <span data-ttu-id="74e27-164">Execute o seguinte comando para interromper o serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-164">Run the following command to stop the service:</span></span>

    <span data-ttu-id="74e27-165">**svccontrol parar SvcName**</span><span class="sxs-lookup"><span data-stu-id="74e27-165">**svccontrol stop SvcName**</span></span>

    <span data-ttu-id="74e27-166">Se a operação for concluída com sucesso, o programa de controle de serviço gravará "serviço interrompido pendente..." e "o serviço foi interrompido com êxito" para o console.</span><span class="sxs-lookup"><span data-stu-id="74e27-166">If the operation succeeds, the service control program writes "Service stop pending..." and then "Service stopped successfully" to the console.</span></span> <span data-ttu-id="74e27-167">Caso contrário, o programa gravará uma mensagem de erro no console.</span><span class="sxs-lookup"><span data-stu-id="74e27-167">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="74e27-168">Se o serviço for interrompido com êxito, o **status** será em branco.</span><span class="sxs-lookup"><span data-stu-id="74e27-168">If the service stops successfully, **Status** is blank.</span></span>

    <span data-ttu-id="74e27-169">Se o serviço não for interrompido, o programa de controle de serviço gravará uma mensagem de erro no log de eventos que inclui o nome da função que falhou e o código de erro que foi retornado em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="74e27-169">If the service fails to stop, the service control program writes an error message to the event log that includes the name of the function that failed and the error code that was returned on failure.</span></span>

10. <span data-ttu-id="74e27-170">Execute o seguinte comando para excluir o serviço:</span><span class="sxs-lookup"><span data-stu-id="74e27-170">Run the following command to delete the service:</span></span>

    <span data-ttu-id="74e27-171">**svcconfig excluir SvcName**</span><span class="sxs-lookup"><span data-stu-id="74e27-171">**svcconfig delete SvcName**</span></span>

    <span data-ttu-id="74e27-172">O programa de configuração de serviço grava "serviço excluído com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="74e27-172">The service configuration program writes "Service deleted successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="74e27-173">Se o serviço for excluído com êxito, ele não será mais exibido no aplicativo de **Serviços** .</span><span class="sxs-lookup"><span data-stu-id="74e27-173">If the service is deleted successfully, it is no longer displayed in the **Services** application.</span></span> <span data-ttu-id="74e27-174">(Observe que se você tentar excluir um serviço que não está parado, a operação terá sucesso, mas o **tipo de inicialização** será definido como "desabilitado" e a entrada de serviço será excluída na reinicialização do sistema ou quando o serviço for encerrado usando o Gerenciador de tarefas.)</span><span class="sxs-lookup"><span data-stu-id="74e27-174">(Note that if you attempt to delete a service that is not stopped, the operation succeeds but **Startup Type** is set to "Disabled" and the service entry will be deleted at system restart or when the service is terminated using Task Manager.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="74e27-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74e27-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74e27-176">Usando serviços</span><span class="sxs-lookup"><span data-stu-id="74e27-176">Using Services</span></span>](using-services.md)
</dt> </dl>

 

 
