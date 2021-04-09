---
description: Os usuários podem configurar a depuração automática para ajudá-los a determinar por que o sistema ou um aplicativo parou de responder.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configurando a depuração automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088854"
---
# <a name="configuring-automatic-debugging"></a><span data-ttu-id="a4886-103">Configurando a depuração automática</span><span class="sxs-lookup"><span data-stu-id="a4886-103">Configuring Automatic Debugging</span></span>

<span data-ttu-id="a4886-104">Os usuários podem configurar a depuração automática para ajudá-los a determinar por que o sistema ou um aplicativo parou de responder.</span><span class="sxs-lookup"><span data-stu-id="a4886-104">Users can configure automatic debugging to help them determine why their system or an application has stopped responding.</span></span>

## <a name="configuring-automatic-debugging-for-system-crashes"></a><span data-ttu-id="a4886-105">Configurando a depuração automática para falhas do sistema</span><span class="sxs-lookup"><span data-stu-id="a4886-105">Configuring Automatic Debugging for System Crashes</span></span>

<span data-ttu-id="a4886-106">Para configurar o computador de destino para gerar um arquivo de despejo de memória quando o sistema parar de responder, use o aplicativo do **sistema** no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="a4886-106">To configure the target computer to generate a crash dump file when the system stops responding, use the **System** application in Control Panel.</span></span> <span data-ttu-id="a4886-107">Clique em **Configurações avançadas do sistema**, que exibe a caixa de diálogo **Propriedades do sistema** .</span><span class="sxs-lookup"><span data-stu-id="a4886-107">Click **Advanced system settings**, which displays the **System Properties** dialog box.</span></span> <span data-ttu-id="a4886-108">Na guia **avançado** da caixa, clique em **configurações** em **inicialização e recuperação** e, em seguida, use as opções de recuperação apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a4886-108">On the **Advanced** tab of that box, click **Settings** under **Startup and Recovery**, and then use the appropriate recovery options.</span></span> <span data-ttu-id="a4886-109">Como alternativa, você pode configurar as opções de despejo de memória usando a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="a4886-109">Alternatively, you can configure crash dump options using the following registry key:</span></span>

<span data-ttu-id="a4886-110">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **CrashControl**</span><span class="sxs-lookup"><span data-stu-id="a4886-110">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

<span data-ttu-id="a4886-111">O arquivo que você pode especificar é o arquivo de despejo de memória.</span><span class="sxs-lookup"><span data-stu-id="a4886-111">The file you can specify is the crash dump file.</span></span> <span data-ttu-id="a4886-112">Seu nome padrão é Memory. dmp.</span><span class="sxs-lookup"><span data-stu-id="a4886-112">Its default name is Memory.dmp.</span></span> <span data-ttu-id="a4886-113">Você pode depurar um despejo de memória com um depurador do modo kernel, como o WinDbg ou o KD.</span><span class="sxs-lookup"><span data-stu-id="a4886-113">You can debug a crash dump with a kernel-mode debugger, such as WinDbg or KD.</span></span> <span data-ttu-id="a4886-114">Para obter mais informações, consulte a documentação incluída com o depurador.</span><span class="sxs-lookup"><span data-stu-id="a4886-114">For more information, see the documentation included with the debugger.</span></span>

## <a name="configuring-automatic-debugging-for-application-crashes"></a><span data-ttu-id="a4886-115">Configurando a depuração automática para falhas do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a4886-115">Configuring Automatic Debugging for Application Crashes</span></span>

<span data-ttu-id="a4886-116">Quando um aplicativo para de responder (por exemplo, após uma violação de acesso), o sistema invoca automaticamente um depurador que é especificado no registro para depuração postmortem, a ID do processo e o identificador de evento são passados para o depurador se a linha de comando estiver configurada corretamente.</span><span class="sxs-lookup"><span data-stu-id="a4886-116">When an application stops responding (for example, after an access violation), the system automatically invokes a debugger that is specified in the registry for postmortem debugging, The process ID and event handle are passed to the debugger if the command line is properly configured.</span></span> <span data-ttu-id="a4886-117">O procedimento a seguir descreve como especificar um depurador no registro.</span><span class="sxs-lookup"><span data-stu-id="a4886-117">The following procedure describes how to specify a debugger in the registry.</span></span>

<span data-ttu-id="a4886-118">**Para definir um depurador como o depurador postmortem**</span><span class="sxs-lookup"><span data-stu-id="a4886-118">**To set a debugger as the postmortem debugger**</span></span>

1.  <span data-ttu-id="a4886-119">Vá para a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="a4886-119">Go to the following registry key:</span></span>

    <span data-ttu-id="a4886-120">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**</span><span class="sxs-lookup"><span data-stu-id="a4886-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="a4886-121">Adicione ou edite o valor do **depurador** usando uma \_ cadeia de caracteres reg sz que especifica a linha de comando para o depurador.</span><span class="sxs-lookup"><span data-stu-id="a4886-121">Add or edit the **Debugger** value, using a REG\_SZ string that specifies the command line for the debugger.</span></span>

    <span data-ttu-id="a4886-122">A cadeia de caracteres deve incluir o caminho totalmente qualificado para o executável do depurador.</span><span class="sxs-lookup"><span data-stu-id="a4886-122">The string should include the fully qualified path to the debugger executable.</span></span> <span data-ttu-id="a4886-123">Indique a ID do processo e o identificador de evento com os parâmetros "% ld" para a linha de comando do depurador.</span><span class="sxs-lookup"><span data-stu-id="a4886-123">Indicate the process ID and event handle with "%ld" parameters to the debugger command line.</span></span> <span data-ttu-id="a4886-124">Depuradores diferentes podem ter suas próprias sintaxes de parâmetro para indicar esses valores.</span><span class="sxs-lookup"><span data-stu-id="a4886-124">Different debuggers may have their own parameter syntaxes for indicating these values.</span></span> <span data-ttu-id="a4886-125">Quando o depurador é invocado, o primeiro "% ld" é substituído pela ID do processo e o segundo "% ld" é substituído pelo identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="a4886-125">When the debugger is invoked, the first "%ld" is replaced with the process ID and the second "%ld" is replaced with the event handle.</span></span>

    <span data-ttu-id="a4886-126">O texto a seguir é um exemplo de como configurar o WinDbg como o depurador.</span><span class="sxs-lookup"><span data-stu-id="a4886-126">The following text is an example of how to setup up WinDbg as the debugger.</span></span>

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  <span data-ttu-id="a4886-127">Se você quiser que o depurador seja invocado sem interação do usuário, adicione ou edite o valor **automático** , usando uma \_ cadeia de caracteres reg sz que especifica se o sistema deve exibir uma caixa de diálogo para o usuário antes do depurador ser invocado.</span><span class="sxs-lookup"><span data-stu-id="a4886-127">If you want the debugger to be invoked without user interaction, add or edit the **Auto** value, using a REG\_SZ string that specifies whether the system should display a dialog box to the user before the debugger is invoked.</span></span> <span data-ttu-id="a4886-128">A cadeia de caracteres "1" desabilita a caixa de diálogo; a cadeia de caracteres "0" habilita a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a4886-128">The string "1" disables the dialog box; the string "0" enables the dialog box.</span></span>

## <a name="excluding-an-application-from-automatic-debugging"></a><span data-ttu-id="a4886-129">Excluindo um aplicativo da depuração automática</span><span class="sxs-lookup"><span data-stu-id="a4886-129">Excluding an Application from Automatic Debugging</span></span>

<span data-ttu-id="a4886-130">O procedimento a seguir descreve como excluir um aplicativo da depuração automática depois que o valor **automático** na chave **AeDebug** tiver sido definido como 1.</span><span class="sxs-lookup"><span data-stu-id="a4886-130">The following procedure describes how to exclude an application from automatic debugging after the **Auto** value under the **AeDebug** key has been set to 1.</span></span>

<span data-ttu-id="a4886-131">**Para excluir um aplicativo da depuração automática**</span><span class="sxs-lookup"><span data-stu-id="a4886-131">**To exclude an application from automatic debugging**</span></span>

1.  <span data-ttu-id="a4886-132">Vá para a seguinte chave do registro:</span><span class="sxs-lookup"><span data-stu-id="a4886-132">Go to the following registry key:</span></span>

    <span data-ttu-id="a4886-133">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**</span><span class="sxs-lookup"><span data-stu-id="a4886-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="a4886-134">Adicione um \_ valor reg DWORD à subchave autodelelist, em que o nome é o nome do arquivo executável e o valor é 1. </span><span class="sxs-lookup"><span data-stu-id="a4886-134">Add a REG\_DWORD value to the **AutoExclusionList** subkey, where the name is the name of the executable file and the value is 1.</span></span> <span data-ttu-id="a4886-135">Por padrão, o Gerenciador de Janelas da Área de Trabalho (Dwm.exe) é excluído da depuração automática porque, caso contrário, um deadlock do sistema pode ocorrer se Dwm.exe para de responder (o usuário não pode ver a interface exibida pelo depurador porque Dwm.exe não está respondendo e Dwm.exe não pode terminar porque ele é mantido pelo depurador).</span><span class="sxs-lookup"><span data-stu-id="a4886-135">By default, the Desktop Window Manager (Dwm.exe) is excluded from automatic debugging because otherwise a system deadlock can occur if Dwm.exe stops responding (the user cannot see the interface displayed by the debugger because Dwm.exe isn't responding, and Dwm.exe cannot terminate because it is held by the debugger).</span></span>

    <span data-ttu-id="a4886-136">**Windows Server 2003 e Windows XP:** A subchave **ExclusionList** não está disponível; Portanto, você não pode excluir nenhum aplicativo, incluindo Dwm.exe, da depuração automática.</span><span class="sxs-lookup"><span data-stu-id="a4886-136">**Windows Server 2003 and Windows XP:** The **AutoExclusionList** subkey is not available; thus you cannot exclude any application, including Dwm.exe, from automatic debugging.</span></span>

<span data-ttu-id="a4886-137">As entradas de registro **AeDebug** padrão podem ser representadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a4886-137">The default **AeDebug** registry entries can be represented as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a><span data-ttu-id="a4886-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4886-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4886-139">Habilitando a depuração do postmortem com o WinDbg</span><span class="sxs-lookup"><span data-stu-id="a4886-139">Enabling Postmortem Debugging with WinDbg</span></span>](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
