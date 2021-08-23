---
description: As ações personalizadas podem adicionar informações de tempo e progresso a um controle ProgressBar. Para obter mais informações sobre como criar uma caixa de diálogo de exibição de ação com um ProgressBar, consulte Criando um controle ProgressBar.
ms.assetid: 101e6b59-3791-450c-9dc6-8930bd665a93
title: Adicionando ações personalizadas ao ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d83dfeb806eb0ed6f1e251dd48b97911d8e0f583c8b65cb48ef0d04df059ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811056"
---
# <a name="adding-custom-actions-to-the-progressbar"></a>Adicionando ações personalizadas ao ProgressBar

As [ações personalizadas](custom-actions.md) podem adicionar informações de tempo e progresso a um controle [ProgressBar](progressbar-control.md) . Para obter mais informações sobre como criar uma caixa de diálogo de exibição de ação com um ProgressBar, consulte Criando [um controle ProgressBar](authoring-a-progressbar-control.md).

observe que duas ações personalizadas devem ser adicionadas ao pacote de Windows Installer para relatar com precisão informações de tempo e progresso ao ProgressBar. Uma ação personalizada deve ser uma ação personalizada adiada. Essa ação personalizada deve concluir a instalação personalizada e enviar as quantidades de incrementos individuais para o controle [ProgressBar](progressbar-control.md) quando o instalador executa o script de instalação. A segunda ação personalizada deve ser uma ação personalizada de execução imediata que informa a ProgressBar quantos tiques adicionar à contagem total durante a fase de aquisição e geração de script da instalação.

**Para adicionar uma ação personalizada ao ProgressBar**

1.  Decida como a ação personalizada descreverá seu progresso. Por exemplo, uma ação personalizada que instala chaves do registro pode exibir uma mensagem de progresso e atualizar o [ProgressBar](progressbar-control.md) toda vez que o instalador grava uma chave do registro.
2.  Cada atualização pela ação personalizada altera o comprimento do [ProgressBar](progressbar-control.md) por um incremento constante. Especifique ou Calcule o número de tiques em cada incremento. Normalmente, uma alteração no tamanho de ProgressBar de um tique corresponde à instalação de um byte. Por exemplo, se o instalador instalar aproximadamente 10000 bytes ao gravar uma chave do registro, você poderá especificar que há 10000 tiques em um incremento.
3.  Especifique ou Calcule o número total de tiques que a ação personalizada adiciona ao comprimento do [ProgressBar](progressbar-control.md). O número de tiques adicionados pela ação personalizada geralmente é calculado como: (incremento de escala) x (número de itens). Por exemplo, se a ação personalizada gravar 10 chaves do registro, o instalador instalará aproximadamente 100000 bytes e o instalador, portanto, deverá aumentar a estimativa do tamanho total final do ProgressBar por 100000 tiques.
    > [!Note]  
    > Para calcular isso dinamicamente, a ação personalizada deve conter uma seção que é executada imediatamente durante a geração de script. A quantidade de tiques relatados pela ação personalizada de execução adiada deve ser igual ao número de tiques adicionados à contagem total de tiques pela ação de execução imediata. Se esse não for o caso, o tempo restante, conforme relatado pelo controle de texto permanecendo, será impreciso.

     

4.  Separe sua ação personalizada em duas seções de código: uma seção que é executada durante a fase de geração de script e uma seção que é executada durante a fase de execução da instalação. Você pode fazer isso usando dois arquivos ou pode usar um arquivo por condicionamento no modo de execução do instalador. O exemplo a seguir usa um arquivo e verifica o estado da instalação. As seções do exemplo são condicionadas para serem executadas dependendo se o instalador está na fase de execução ou geração de script da instalação.
5.  A seção que é executada durante a geração de script deve aumentar a estimativa do tamanho total final do [ProgressBar](progressbar-control.md) pelo número total de tiques na ação personalizada. Isso é feito enviando uma mensagem de progresso **ProgressAddition** .
6.  A seção que é executada durante a fase de execução da instalação deve configurar o texto e os modelos da mensagem para informar ao usuário sobre o que a ação personalizada está fazendo e para direcionar o instalador na atualização do controle [ProgressBar](progressbar-control.md) . Por exemplo, informe o instalador para mover o ProgressBar para frente um incremento e enviar uma mensagem de progresso explícita com cada atualização. Geralmente, há um loop nesta seção se a ação personalizada estiver instalando algo. Com cada passagem desse loop, o instalador pode instalar um item de referência, como uma chave do registro, e atualizar o controle ProgressBar
7.  adicione uma ação personalizada de execução imediata ao seu pacote de Windows Installer. Essa ação personalizada informa o [ProgressBar](progressbar-control.md) quanto avançar durante as fases de aquisição e geração de script da instalação. Para o exemplo a seguir, a origem é a DLL criada pela compilação do código de exemplo e o destino é o ponto de entrada, CAProgress.
8.  adicione uma ação personalizada de execução adiada ao seu pacote de Windows Installer. Essa ação personalizada conclui as etapas da instalação real e informa o [ProgressBar](progressbar-control.md) quanto para avançar a barra no momento em que o instalador executa o script de instalação. Para o exemplo a seguir, a origem é a DLL criada pela compilação do código de exemplo e o destino é o ponto de entrada, CAProgress.
9.  Agende as ações personalizadas entre [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) na tabela [InstallExecuteSequence](installexecutesequence-table.md) . A ação personalizada adiada deve ser agendada imediatamente após a ação personalizada de execução imediata. O instalador não executará a ação personalizada adiada até que o script seja executado.

O exemplo a seguir mostra como uma ação personalizada pode ser adicionada ao [ProgressBar](progressbar-control.md). A origem de ambas as ações personalizadas é a DLL criada pela compilação do código de exemplo e o destino de ambas as ações personalizadas é o ponto de entrada, CAProgress. Este exemplo não faz nenhuma alteração real no sistema, mas opera o ProgressBar como se estiver instalando 10 itens de referência com aproximadamente 10.000 bytes de tamanho. O instalador atualiza a mensagem e a ProgressBar sempre que instala um item de referência.


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



 

 



