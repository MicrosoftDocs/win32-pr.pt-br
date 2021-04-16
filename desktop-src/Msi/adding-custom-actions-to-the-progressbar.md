---
description: As ações personalizadas podem adicionar informações de tempo e progresso a um controle ProgressBar. Para obter mais informações sobre como criar uma caixa de diálogo de exibição de ação com um ProgressBar, consulte Criando um controle ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Adicionando ações personalizadas ao ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff2b6da9e72a37329b26cfce7590bab5f9792db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750257"
---
# <a name="adding-custom-actions-to-the-progressbar"></a><span data-ttu-id="69cc8-104">Adicionando ações personalizadas ao ProgressBar</span><span class="sxs-lookup"><span data-stu-id="69cc8-104">Adding Custom Actions to the ProgressBar</span></span>

<span data-ttu-id="69cc8-105">As [ações personalizadas](custom-actions.md) podem adicionar informações de tempo e progresso a um controle [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="69cc8-105">[Custom Actions](custom-actions.md) can add time and progress information to a [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="69cc8-106">Para obter mais informações sobre como criar uma caixa de diálogo de exibição de ação com um ProgressBar, consulte Criando [um controle ProgressBar](authoring-a-progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="69cc8-106">For more information about creating an action display dialog box having a ProgressBar, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md).</span></span>

<span data-ttu-id="69cc8-107">Observe que duas ações personalizadas devem ser adicionadas ao pacote de Windows Installer para relatar com precisão informações de tempo e progresso ao ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="69cc8-107">Note that two custom actions must be added to the Windows Installer package to accurately report time and progress information to the ProgressBar.</span></span> <span data-ttu-id="69cc8-108">Uma ação personalizada deve ser uma ação personalizada adiada.</span><span class="sxs-lookup"><span data-stu-id="69cc8-108">One custom action must be a deferred custom action.</span></span> <span data-ttu-id="69cc8-109">Essa ação personalizada deve concluir a instalação personalizada e enviar as quantidades de incrementos individuais para o controle [ProgressBar](progressbar-control.md) quando o instalador executa o script de instalação.</span><span class="sxs-lookup"><span data-stu-id="69cc8-109">This custom action should complete your custom installation and send the amounts of individual increments to the [ProgressBar](progressbar-control.md) control when the installer runs the installation script.</span></span> <span data-ttu-id="69cc8-110">A segunda ação personalizada deve ser uma ação personalizada de execução imediata que informa a ProgressBar quantos tiques adicionar à contagem total durante a fase de aquisição e geração de script da instalação.</span><span class="sxs-lookup"><span data-stu-id="69cc8-110">The second custom action must be an immediate execution custom action that informs the ProgressBar how many ticks to add to the total count during the acquisition and script generation phase of the installation.</span></span>

<span data-ttu-id="69cc8-111">**Para adicionar uma ação personalizada ao ProgressBar**</span><span class="sxs-lookup"><span data-stu-id="69cc8-111">**To add a custom action to the ProgressBar**</span></span>

1.  <span data-ttu-id="69cc8-112">Decida como a ação personalizada descreverá seu progresso.</span><span class="sxs-lookup"><span data-stu-id="69cc8-112">Decide how the custom action will describe its progress.</span></span> <span data-ttu-id="69cc8-113">Por exemplo, uma ação personalizada que instala chaves do registro pode exibir uma mensagem de progresso e atualizar o [ProgressBar](progressbar-control.md) toda vez que o instalador grava uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="69cc8-113">For example, a custom action that installs registry keys could display a progress message and update the [ProgressBar](progressbar-control.md) each time the installer writes one registry key.</span></span>
2.  <span data-ttu-id="69cc8-114">Cada atualização pela ação personalizada altera o comprimento do [ProgressBar](progressbar-control.md) por um incremento constante.</span><span class="sxs-lookup"><span data-stu-id="69cc8-114">Each update by the custom action changes the length of the [ProgressBar](progressbar-control.md) by a constant increment.</span></span> <span data-ttu-id="69cc8-115">Especifique ou Calcule o número de tiques em cada incremento.</span><span class="sxs-lookup"><span data-stu-id="69cc8-115">Specify or calculate the number of ticks in each increment.</span></span> <span data-ttu-id="69cc8-116">Normalmente, uma alteração no tamanho de ProgressBar de um tique corresponde à instalação de um byte.</span><span class="sxs-lookup"><span data-stu-id="69cc8-116">Typically a change in ProgressBar length of one tick corresponds to the installation of one byte.</span></span> <span data-ttu-id="69cc8-117">Por exemplo, se o instalador instalar aproximadamente 10000 bytes ao gravar uma chave do registro, você poderá especificar que há 10000 tiques em um incremento.</span><span class="sxs-lookup"><span data-stu-id="69cc8-117">For example, if the installer installs approximately 10000 bytes when it writes one registry key, you can specify that there are 10000 ticks in an increment.</span></span>
3.  <span data-ttu-id="69cc8-118">Especifique ou Calcule o número total de tiques que a ação personalizada adiciona ao comprimento do [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="69cc8-118">Specify or calculate the total number of ticks the custom action adds to the length of the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="69cc8-119">O número de tiques adicionados pela ação personalizada geralmente é calculado como: (incremento de escala) x (número de itens).</span><span class="sxs-lookup"><span data-stu-id="69cc8-119">The number of ticks added by the custom action is usually calculated as: (tick increment) x (number of items).</span></span> <span data-ttu-id="69cc8-120">Por exemplo, se a ação personalizada gravar 10 chaves do registro, o instalador instalará aproximadamente 100000 bytes e o instalador, portanto, deverá aumentar a estimativa do tamanho total final do ProgressBar por 100000 tiques.</span><span class="sxs-lookup"><span data-stu-id="69cc8-120">For example, if the custom action writes 10 registry keys, the installer installs approximately 100000 bytes and the installer therefore must increase the estimate of the final total length of the ProgressBar by 100000 ticks.</span></span>
    > [!Note]  
    > <span data-ttu-id="69cc8-121">Para calcular isso dinamicamente, a ação personalizada deve conter uma seção que é executada imediatamente durante a geração de script.</span><span class="sxs-lookup"><span data-stu-id="69cc8-121">To calculate this dynamically, the custom action must contain a section that is immediately executed during script generation.</span></span> <span data-ttu-id="69cc8-122">A quantidade de tiques relatados pela ação personalizada de execução adiada deve ser igual ao número de tiques adicionados à contagem total de tiques pela ação de execução imediata.</span><span class="sxs-lookup"><span data-stu-id="69cc8-122">The amount of ticks reported by your deferred execution custom action must be equal to the number of ticks added to the total tick count by the immediate execution action.</span></span> <span data-ttu-id="69cc8-123">Se esse não for o caso, o tempo restante, conforme relatado pelo controle de texto permanecendo, será impreciso.</span><span class="sxs-lookup"><span data-stu-id="69cc8-123">If this is not the case, the time remaining as reported by the TimeRemaining text control will be inaccurate.</span></span>

     

4.  <span data-ttu-id="69cc8-124">Separe sua ação personalizada em duas seções de código: uma seção que é executada durante a fase de geração de script e uma seção que é executada durante a fase de execução da instalação.</span><span class="sxs-lookup"><span data-stu-id="69cc8-124">Separate your custom action into two sections of code: a section that runs during the script generation phase and a section that runs during the execution phase of the installation.</span></span> <span data-ttu-id="69cc8-125">Você pode fazer isso usando dois arquivos ou pode usar um arquivo por condicionamento no modo de execução do instalador.</span><span class="sxs-lookup"><span data-stu-id="69cc8-125">You can do this using two files or you can use one file by conditioning on the run mode of the installer.</span></span> <span data-ttu-id="69cc8-126">O exemplo a seguir usa um arquivo e verifica o estado da instalação.</span><span class="sxs-lookup"><span data-stu-id="69cc8-126">The following sample uses one file and checks the installation state.</span></span> <span data-ttu-id="69cc8-127">As seções do exemplo são condicionadas para serem executadas dependendo se o instalador está na fase de execução ou geração de script da instalação.</span><span class="sxs-lookup"><span data-stu-id="69cc8-127">Sections of the sample are conditioned to run depending on whether the installer is in the execution or script generation phase of the installation.</span></span>
5.  <span data-ttu-id="69cc8-128">A seção que é executada durante a geração de script deve aumentar a estimativa do tamanho total final do [ProgressBar](progressbar-control.md) pelo número total de tiques na ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="69cc8-128">The section that runs during script generation should increase the estimate of the final total length of the [ProgressBar](progressbar-control.md) by the total number of ticks in the custom action.</span></span> <span data-ttu-id="69cc8-129">Isso é feito enviando uma mensagem de progresso **ProgressAddition** .</span><span class="sxs-lookup"><span data-stu-id="69cc8-129">This is done by sending a **ProgressAddition** progress message.</span></span>
6.  <span data-ttu-id="69cc8-130">A seção que é executada durante a fase de execução da instalação deve configurar o texto e os modelos da mensagem para informar ao usuário sobre o que a ação personalizada está fazendo e para direcionar o instalador na atualização do controle [ProgressBar](progressbar-control.md) .</span><span class="sxs-lookup"><span data-stu-id="69cc8-130">The section that runs during the execution phase of installation should set up message text and templates to inform the user about what the custom action is doing and to direct the installer on updating the [ProgressBar](progressbar-control.md) control.</span></span> <span data-ttu-id="69cc8-131">Por exemplo, informe o instalador para mover o ProgressBar para frente um incremento e enviar uma mensagem de progresso explícita com cada atualização.</span><span class="sxs-lookup"><span data-stu-id="69cc8-131">For example, inform the installer to move the ProgressBar forward one increment and send an explicit progress message with each update.</span></span> <span data-ttu-id="69cc8-132">Geralmente, há um loop nesta seção se a ação personalizada estiver instalando algo.</span><span class="sxs-lookup"><span data-stu-id="69cc8-132">There is usually a loop in this section if the custom action is installing something.</span></span> <span data-ttu-id="69cc8-133">Com cada passagem desse loop, o instalador pode instalar um item de referência, como uma chave do registro, e atualizar o controle ProgressBar</span><span class="sxs-lookup"><span data-stu-id="69cc8-133">With each pass through this loop, the installer can install one reference item such as a registry key and update the ProgressBar control</span></span>
7.  <span data-ttu-id="69cc8-134">Adicione uma ação personalizada de execução imediata ao seu pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="69cc8-134">Add an immediate execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="69cc8-135">Essa ação personalizada informa o [ProgressBar](progressbar-control.md) quanto avançar durante as fases de aquisição e geração de script da instalação.</span><span class="sxs-lookup"><span data-stu-id="69cc8-135">This custom action informs the [ProgressBar](progressbar-control.md) how much to advance during the aquisition and script generation phases of the installation.</span></span> <span data-ttu-id="69cc8-136">Para o exemplo a seguir, a origem é a DLL criada pela compilação do código de exemplo e o destino é o ponto de entrada, CAProgress.</span><span class="sxs-lookup"><span data-stu-id="69cc8-136">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
8.  <span data-ttu-id="69cc8-137">Adicione uma ação personalizada de execução adiada ao seu pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="69cc8-137">Add a deferred execution custom action to your Windows Installer package.</span></span> <span data-ttu-id="69cc8-138">Essa ação personalizada conclui as etapas da instalação real e informa o [ProgressBar](progressbar-control.md) quanto para avançar a barra no momento em que o instalador executa o script de instalação.</span><span class="sxs-lookup"><span data-stu-id="69cc8-138">This custom action completes the steps of the actual installation and informs the [ProgressBar](progressbar-control.md) how much to advance the bar at the time when the installer runs the installation script.</span></span> <span data-ttu-id="69cc8-139">Para o exemplo a seguir, a origem é a DLL criada pela compilação do código de exemplo e o destino é o ponto de entrada, CAProgress.</span><span class="sxs-lookup"><span data-stu-id="69cc8-139">For the following sample, the source is the DLL created by compiling the sample code and the target is the entry point, CAProgress.</span></span>
9.  <span data-ttu-id="69cc8-140">Agende as ações personalizadas entre [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) na tabela [InstallExecuteSequence](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="69cc8-140">Schedule both custom actions between [InstallInitialize](installinitialize-action.md) and [InstallFinalize](installfinalize-action.md) in the [InstallExecuteSequence](installexecutesequence-table.md) table.</span></span> <span data-ttu-id="69cc8-141">A ação personalizada adiada deve ser agendada imediatamente após a ação personalizada de execução imediata.</span><span class="sxs-lookup"><span data-stu-id="69cc8-141">The deferred custom action should be scheduled immediately after the immediate execution custom action.</span></span> <span data-ttu-id="69cc8-142">O instalador não executará a ação personalizada adiada até que o script seja executado.</span><span class="sxs-lookup"><span data-stu-id="69cc8-142">The installer will not run the deferred custom action until the script is executed.</span></span>

<span data-ttu-id="69cc8-143">O exemplo a seguir mostra como uma ação personalizada pode ser adicionada ao [ProgressBar](progressbar-control.md).</span><span class="sxs-lookup"><span data-stu-id="69cc8-143">The following sample shows how a custom action can be added to the [ProgressBar](progressbar-control.md).</span></span> <span data-ttu-id="69cc8-144">A origem de ambas as ações personalizadas é a DLL criada pela compilação do código de exemplo e o destino de ambas as ações personalizadas é o ponto de entrada, CAProgress.</span><span class="sxs-lookup"><span data-stu-id="69cc8-144">The source of both custom actions is the DLL created by compiling the sample code and the target of both custom actions is the entry point, CAProgress.</span></span> <span data-ttu-id="69cc8-145">Este exemplo não faz nenhuma alteração real no sistema, mas opera o ProgressBar como se estiver instalando 10 itens de referência com aproximadamente 10.000 bytes de tamanho.</span><span class="sxs-lookup"><span data-stu-id="69cc8-145">This sample does not make any actual changes to the system, but operates the ProgressBar as if installing 10 reference items that are each approximately 10,000 bytes in size.</span></span> <span data-ttu-id="69cc8-146">O instalador atualiza a mensagem e a ProgressBar sempre que instala um item de referência.</span><span class="sxs-lookup"><span data-stu-id="69cc8-146">The installer updates the message and ProgressBar each time it installs a reference item.</span></span>


```C++
#include <windows.h>
#include <msiquery.h>
#pragma comment(lib, "msi.lib")

// Specify or calculate the number of ticks in an increment
// to the ProgressBar
const UINT iTickIncrement = 10000;
 
// Specify or calculate the total number of ticks the custom 
// action adds to the length of the ProgressBar
const UINT iNumberItems = 10;
const UINT iTotalTicks = iTickIncrement * iNumberItems;
 
UINT __stdcall CAProgress(MSIHANDLE hInstall)
{
    // Tell the installer to check the installation state and execute
    // the code needed during the rollback, acquisition, or
    // execution phases of the installation.
  
    if (MsiGetMode(hInstall,MSIRUNMODE_SCHEDULED) == TRUE)
    {
        PMSIHANDLE hActionRec = MsiCreateRecord(3);
        PMSIHANDLE hProgressRec = MsiCreateRecord(3);

        // Installer is executing the installation script. Set up a
        // record specifying appropriate templates and text for
        // messages that will inform the user about what the custom
        // action is doing. Tell the installer to use this template and 
        // text in progress messages.
 
        MsiRecordSetString(hActionRec, 1, TEXT("MyCustomAction"));
        MsiRecordSetString(hActionRec, 2, TEXT("Incrementing the Progress Bar..."));
        MsiRecordSetString(hActionRec, 3, TEXT("Incrementing tick [1] of [2]"));
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONSTART, hActionRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        // Tell the installer to use explicit progress messages.
        MsiRecordSetInteger(hProgressRec, 1, 1);
        MsiRecordSetInteger(hProgressRec, 2, 1);
        MsiRecordSetInteger(hProgressRec, 3, 0);
        iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
        if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;
              
        //Specify that an update of the progress bar's position in
        //this case means to move it forward by one increment.
        MsiRecordSetInteger(hProgressRec, 1, 2);
        MsiRecordSetInteger(hProgressRec, 2, iTickIncrement);
        MsiRecordSetInteger(hProgressRec, 3, 0);
 
        // The following loop sets up the record needed by the action
        // messages and tells the installer to send a message to update
        // the progress bar.

        MsiRecordSetInteger(hActionRec, 2, iTotalTicks);
       
        for( int i = 0; i < iTotalTicks; i+=iTickIncrement)
        {
            MsiRecordSetInteger(hActionRec, 1, i);

            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_ACTIONDATA, hActionRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
          
            iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
            if ((iResult == IDCANCEL))
                return ERROR_INSTALL_USEREXIT;
   
            //A real custom action would have code here that does a part
            //of the installation. For this sample, code that installs
            //10 registry keys.
            Sleep(1000);
                    
        }
        return ERROR_SUCCESS;
    }
    else
    {
        // Installer is generating the installation script of the
        // custom action.
  
        // Tell the installer to increase the value of the final total
        // length of the progress bar by the total number of ticks in
        // the custom action.
        PMSIHANDLE hProgressRec = MsiCreateRecord(2);

         MsiRecordSetInteger(hProgressRec, 1, 3);
            MsiRecordSetInteger(hProgressRec, 2, iTotalTicks);
        UINT iResult = MsiProcessMessage(hInstall, INSTALLMESSAGE_PROGRESS, hProgressRec);
           if ((iResult == IDCANCEL))
            return ERROR_INSTALL_USEREXIT;     
        return ERROR_SUCCESS;
     }
}
```



 

 



