---
description: As IDs do Modelo de Usuário do Aplicativo (AppUserModelIDs) são amplamente usadas pela barra de tarefas no Windows 7 e sistemas posteriores para associar processos, arquivos e janelas a um aplicativo específico.
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: IDs de modelo de usuário do aplicativo (AppUserModelIDs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd0835af241a36e4d9c95237890cb63790f7fe9031476dfa8ec21254266ffd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351466"
---
# <a name="application-user-model-ids-appusermodelids"></a>IDs de modelo de usuário do aplicativo (AppUserModelIDs)

As IDs do Modelo de Usuário do Aplicativo (AppUserModelIDs) são amplamente usadas pela barra de tarefas no Windows 7 e sistemas posteriores para associar processos, arquivos e janelas a um aplicativo específico. Em alguns casos, é suficiente contar com o AppUserModelID interno atribuído a um processo pelo sistema. No entanto, um aplicativo que possui vários processos ou um aplicativo em execução em um processo de host pode precisar identificar-se explicitamente para que ele possa agrupar suas janelas diferentes em um único botão de barra de tarefas e controlar o conteúdo do Lista de Atalhos.

-   [Application-Defined e System-Defined AppUserModelIDs](#application-defined-and-system-defined-appusermodelids)
-   [Como formar um Application-Defined AppUserModelID](#how-to-form-an-application-defined-appusermodelid)
-   [Onde atribuir um AppUserModelID](#where-to-assign-an-appusermodelid)
-   [Registrando um aplicativo como um processo de host](#registering-an-application-as-a-host-process)
-   [Listas de exclusão para a pinagem da barra de tarefas e listas recentes/frequentes](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [Tópicos relacionados](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined e System-Defined AppUserModelIDs

Alguns aplicativos não declaram um AppUserModelID explícito. Eles são opcionais. Nesse caso, o sistema usa uma série de heurísticas para atribuir um AppUserModelID interno. No entanto, há um benefício de desempenho ao evitar esses cálculos e um AppUserModelID explícito é a única maneira de garantir uma experiência exata do usuário. Portanto, é altamente recomendável que uma ID explícita seja definida. Os aplicativos não podem recuperar um AppUserModelID atribuído pelo sistema.

Se um aplicativo usar um AppUserModelID explícito, ele também deverá atribuir o mesmo AppUserModelID a todas as janelas ou processos em execução, atalhos e associações de arquivo. Ele também deve usar esse AppUserModelID ao personalizar seu Lista de Atalhos por meio de [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)e em qualquer chamada para [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

> [!Note]  
> Se os aplicativos não têm um AppUserModelID explícito, eles devem chamar os métodos [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations), [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)e [**ICustomDestinationList,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) bem como [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) de dentro do aplicativo. Se esses métodos são chamados de outro processo, como um instalador ou desinstalador, o sistema não pode gerar o AppUserModelID correto e essas chamadas não terão efeito.

 

Os itens a seguir descrevem cenários comuns que exigem um AppUserModelID explícito. Eles também apontam casos em que vários AppUserModelIDs explícitos devem ser usados.

-   Um único arquivo executável com uma interface do usuário com vários modos que aparecem para o usuário como aplicativos separados deve atribuir diferentes AppUserModelIDs a cada modo. Por exemplo, uma parte de um aplicativo que os usuários veem como uma experiência independente que eles podem fixar e iniciar na barra de tarefas separadamente do restante do aplicativo deve ter seu próprio AppUserModelID, separado da experiência principal.
-   Vários atalhos com argumentos diferentes que levam ao que o usuário vê como o mesmo aplicativo devem usar um AppUserModelID para todos os atalhos. Por exemplo, Windows Internet Explorer tem atalhos diferentes para modos diferentes (como iniciar sem complementos), mas todos eles devem aparecer para o usuário como uma única instância de Internet Explorer.
-   Um executável que atua como um processo de host e executa o conteúdo de destino como um aplicativo deve se registrar como um aplicativo [host,](#registering-an-application-as-a-host-process)após o qual ele pode atribuir diferentes AppUserModelIDs a cada experiência percebida que ele hospeda. Como alternativa, o processo de host pode permitir que o programa hospedado defina seus AppUserModelIDs. Em ambos os casos, o processo de host deve manter um registro da origem dos AppUserModelIDs, seja ele mesmo ou o aplicativo hospedado. Nesse caso, não há nenhuma experiência de usuário principal do processo de host sem o conteúdo de destino. Exemplos são Windows aplicativos RAIL (Remote Applications Integrated Locally), Java Runtime, RunDLL32.exe ou DLLHost.exe.

    No caso de aplicativos hospedados existentes, o sistema tenta identificar experiências individuais, mas novos aplicativos devem usar AppUserModelIDs explícitos para garantir a experiência do usuário pretendida.

-   Processos cooperativos ou encadeados que para o usuário fazem parte do mesmo aplicativo devem ter o mesmo AppUserModelID aplicado a cada processo. Exemplos incluem jogos com um processo de lançamento (encadeado) e o Microsoft Windows Media Player, que tem uma experiência de primeira execução/configuração em execução em um processo e o aplicativo principal em execução em outro processo (cooperativo).
-   Uma extensão de namespace do Shell que atua como um aplicativo separado para mais do que navegar e gerenciar conteúdo no Windows Explorer deve atribuir um AppUserModelID em suas propriedades de pasta. Um exemplo é o Painel de Controle.
-   Em um ambiente de virtualização, como uma estrutura de implantação, o ambiente de virtualização deve atribuir diferentes AppUserModelIDs a cada aplicativo que gerencia. Nesses casos, um launcher de aplicativo usa um processo intermediário para configurar o ambiente e, em seguida, entrega a operação para um processo diferente para executar o aplicativo. Observe que isso faz com que o sistema não consiga relacionar o processo de destino em execução de volta ao atalho porque o atalho aponta para o processo intermediário.

    Se qualquer aplicativo tiver várias janelas, atalhos ou processos, o AppUserModelID atribuído desse aplicativo também deverá ser aplicado a cada uma dessas partes pelo ambiente de virtualização.

    Um exemplo dessa situação é a estrutura ClickOnce, que atribui corretamente AppUserModelIDs em nome dos aplicativos que gerencia. Assim como em todos esses ambientes, os aplicativos implantados e gerenciados pelo ClickOnce não devem atribuir AppUserModelIDs explícitos em si, pois isso entrará em conflito com os AppUserModelIDs atribuídos pelo ClickOnce e levarão a resultados inesperados.

## <a name="how-to-form-an-application-defined-appusermodelid"></a>Como formar um Application-Defined AppUserModelID

Um aplicativo deve fornecer seu AppUserModelID no formulário a seguir. Ele não pode ter mais de 128 caracteres e não pode conter espaços. Cada seção deve ser em caso de pascal.

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` e `ProductName` sempre devem ser usados, enquanto as partes e são `SubProduct` `VersionInformation` opcionais e dependem dos requisitos do aplicativo. `SubProduct` permite que um aplicativo principal que consiste em várias subaplicações forneça um botão de barra de tarefas separado para cada subaplicação e suas janelas associadas. `VersionInformation` permite que duas versões de um aplicativo coexistam enquanto são vistas como entidades discretas. Se um aplicativo não se destina a ser usado dessa forma, o deve ser omitido para que uma versão atualizada possa usar o mesmo AppUserModelID que a versão que `VersionInformation` ele substituiu.

## <a name="where-to-assign-an-appusermodelid"></a>Onde atribuir um AppUserModelID

Quando um aplicativo usa um ou mais AppUserModelIDs explícitos, ele deve aplicar esses AppUserModelIDs nos seguintes locais e situações:

-   Na [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) do arquivo de atalho do aplicativo. Um atalho (como um [**ShellLink IShellLink,**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)CLSID ShellLink ou um arquivo .lnk) dá suporte a propriedades por meio de \_ [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) e outros mecanismos de configuração de propriedade usados em todo o Shell. Isso permite que a barra de tarefas identifique o atalho apropriado para fixar e garante que as janelas que pertencem ao processo sejam adequadamente associadas a esse botão de barra de tarefas.
    > [!Note]  
    > A [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) deve ser aplicada a um atalho quando esse atalho é criado. Ao usar o Microsoft Windows Installer (MSI) para instalar o aplicativo, a tabela [MsiShortcutProperty](../msi/msishortcutproperty-table.md) permite que o AppUserModelID seja aplicado ao atalho quando ele é criado durante a instalação.

     

-   Como uma propriedade de qualquer uma das janelas em execução do aplicativo. Isso pode ser definido de uma das duas maneiras:

    1.  Se janelas diferentes pertencentes a um processo exigirem Diferentes AppUserModelIDs para controlar o grupo de barras de tarefas, use [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) para recuperar o repositório de propriedades da janela e definir o AppUserModelID como uma propriedade de janela.
    2.  Se todas as janelas no processo usarem o mesmo AppUserModelID, defina AppUserModelID no processo, embora [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid). Um aplicativo deve chamar **SetCurrentProcessExplicitAppUserModelID** para definir seu AppUserModelID durante a rotina de inicialização inicial de um aplicativo antes que o aplicativo apresente qualquer interface do usuário, faça qualquer manipulação de suas Listas de Saltos ou faça (ou faça com que o sistema faça) qualquer chamada para [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

    Um AppUserModelID no nível da janela substitui um AppUserModelID no nível do processo.

    Quando um aplicativo define um AppUserModelID explícito no nível da janela, o aplicativo pode fornecer as especificações de seu comando de relançamento para seu botão de barra de tarefas. Para fornecer essas informações, as seguintes propriedades são usadas:

    -   [System.AppUserModel.RelaunchCommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [System.AppUserModel.RelaunchDisplayNameResource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [System.AppUserModel.RelaunchIconResource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > Se houver um atalho para iniciar o aplicativo, um aplicativo deverá aplicar o AppUserModelID como uma propriedade do atalho em vez de usar as propriedades de relançamento. Nesse caso, a linha de comando, o ícone e o texto do atalho são usados para fornecer as mesmas informações que as propriedades de relançamento.

     

    Um AppUserModelID explícito no nível da janela também pode usar a propriedade [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) para especificar que ela não deve estar disponível para fixar ou relançar.

-   Em uma chamada para personalizar ou atualizar ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)), recupere ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) ou limpe ([**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)) o Lista de Atalhos.
-   No registro de associação de arquivo (por meio de seu  [ProgID](fa-progids.md)) se o aplicativo usar as listas de destino Recentes ou **Frequentes** geradas automaticamente pelo sistema. Essas informações de associação são referenciadas [**por SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Essas informações também são usadas ao adicionar [**destinos IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) a listas de salto personalizadas por [**meio de ICustomDestinationList::AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory).
-   Em qualquer chamada que o aplicativo faz diretamente para [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Se o aplicativo depender da caixa de diálogo de arquivo comum para fazer chamadas para **SHAddToRecentDocs** em seu nome, essas chamadas poderão deduzir o AppUserModelID explícito somente se o AppUserModelID estiver definido para todo o processo. Se o aplicativo define AppUserModelIDs em suas janelas em vez de no processo, o aplicativo deve fazer todas as chamadas para **SHAddToRecentDocs** em si, com seu AppUserModelID explícito, bem como impedir que a caixa de diálogo de arquivo comum faça suas próprias chamadas. Isso deve ser feito sempre que um  item  for aberto, para garantir que as seções Recentes ou Frequentes do Lista de Atalhos do aplicativo sejam precisas.

Os itens a seguir descrevem cenários comuns e onde aplicar AppUserModelIDs explícitos nesses cenários.

-   Quando um único processo contiver vários aplicativos, use [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e definir o AppUserModelID como uma propriedade de janela.
-   Quando um aplicativo usa vários processos, aplique o AppUserModelID a cada processo. Se você usa o mesmo AppUserModelID em cada processo depende se você deseja que cada processo apareça como parte do aplicativo principal ou como entidades individuais.
-   Para separar determinadas janelas de um conjunto no mesmo processo, use o armazenamento de propriedades da janela para aplicar um único AppUserModelID às janelas que você deseja separar e, em seguida, aplique um AppUserModelID diferente ao processo. Qualquer janela nesse processo que não foi rotulada explicitamente com o AppUserModelID no nível da janela herda o AppUserModelID do processo.
-   Se um tipo de arquivo estiver associado a um aplicativo, atribua o AppUserModelID no registro [ProgID](fa-progids.md) do tipo de arquivo. Se um único arquivo executável for lançado em modos diferentes que aparecem para o usuário como aplicativos distintos, um AppUserModelID separado será necessário para cada modo. Nesse caso, deve haver vários registros ProgID para o tipo de arquivo, cada um com um AppUserModelID diferente.
-   Quando há vários locais de atalho dos quais um usuário pode iniciar um aplicativo (no **menu** Iniciar, na área de trabalho ou em outro lugar), recupere o armazenamento de propriedades do atalho para aplicar um único AppUserModelID a todos os atalhos como propriedades de atalho.
-   Quando uma chamada explícita for feita a [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) por um aplicativo, use o AppUserModelID na chamada. Quando a caixa de diálogo de arquivo comum é usada para abrir ou salvar arquivos, **SHAddToRecentDocs** é chamado pela caixa de diálogo em nome do aplicativo. Essa chamada pode inferir o AppUserModelID explícito do processo. No entanto, se um AppUserModelID explícito for aplicado como uma propriedade de janela, a caixa de diálogo de arquivo comum não poderá determinar o AppUserModelID correto. Nesse caso, o próprio aplicativo deve chamar **explicitamente SHAddToRecentDocs** e formorá-lo com o AppUserModelID correto. Além disso, o aplicativo deve impedir que a caixa de diálogo de arquivo comum chamar **SHAddToRecentDocs** em seu nome definindo o sinalizador FOS \_ DONTADDTORECENT no método **GetOptions** [**de IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) [**ou IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog).

## <a name="registering-an-application-as-a-host-process"></a>Registrando um aplicativo como um processo de host

Um aplicativo pode definir a entrada do Registro IsHostApp para fazer com que o processo desse executável seja considerado um processo de host pela barra de tarefas. Isso afeta seu grupo e as entradas Lista de Atalhos padrão.

O exemplo a seguir mostra a entrada do Registro necessária. Observe que a entrada não recebe um valor; sua presença é tudo o que é necessário. É um valor REG \_ NULL.

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

Se o próprio processo ou o arquivo de atalho usado para iniciar o processo tiver um AppUserModelID explícito, a lista de processos do host será ignorada e o aplicativo será tratado como um aplicativo normal pela barra de tarefas. As janelas em execução do aplicativo são agrupadas em um único botão de barra de tarefas e o aplicativo pode ser fixado na barra de tarefas.

Se apenas o nome executável do processo em execução for conhecido, sem um AppUserModelID explícito e esse executável estiver na lista de processos de host, cada instância do processo será tratada como uma entidade separada para o grupo de barras de tarefas. O botão da barra de tarefas associado a qualquer instância específica do processo não exibe uma opção de fixar/fixar ou um ícone de lançamento para uma nova instância do processo. O processo também não está qualificado para inclusão na lista MFU (Uso Mais Usado) do **menu** Iniciar. No entanto, se o processo foi lançado por meio de um atalho que contém argumentos de lançamento (geralmente o conteúdo de destino a ser hospedado como o "aplicativo"), o sistema pode determinar a identidade e o aplicativo pode ser fixado e relançado.

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>Listas de exclusão para a pinagem da barra de tarefas e listas recentes/frequentes

Aplicativos, processos e janelas podem optar por se tornar indisponíveis para fixar na barra de tarefas ou para inclusão na lista MFU do **menu** Iniciar. Há três mecanismos para fazer isso:

1.  Adicione a entrada NoStartPage ao registro do aplicativo, conforme mostrado aqui:

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Os dados associados à entrada NoStartPage são ignorados. Somente a presença da entrada é necessária. Portanto, o tipo ideal para NoStartPage é REG \_ NONE.

    Observe que qualquer uso de um AppUserModelID explícito substitui a entrada NoStartPage. Se um AppUserModelID explícito for aplicado a um atalho, processo ou janela, ele se tornará fixável e qualificado para a lista MFU **do** menu Iniciar.

2.  Defina [a propriedade System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) em janelas e atalhos. Essa propriedade deve ser definida em uma janela antes da [propriedade PKEY \_ AppUserModel \_ ID.](../properties/props-system-appusermodel-id.md)
3.  Adicione um AppUserModelID explícito como um valor na seguinte sub-chave do Registro, conforme mostrado aqui:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Cada entrada é um valor REG \_ NULL com o nome do AppUserModelID. Qualquer AppUserModelID encontrado nesta lista não é fixável e não está qualificado para inclusão na lista Iniciar **menu** MFU.

Esteja ciente de que determinados arquivos executáveis, bem como atalhos que contêm determinadas cadeias de caracteres em seu nome, são excluídos automaticamente da fixar e incluir na lista MFU.

> [!Note]  
> Essa exclusão automática pode ser substituído aplicando um AppUserModelID explícito.

 

Se qualquer uma das cadeias de caracteres a seguir, independentemente do caso, estiver incluída no nome do atalho, o programa não será fixável e não será exibido na lista usada com mais frequência (não aplicável ao Windows 10):

-   Documentação
-   Ajuda
-   Instalar
-   Mais informações
-   Leia-me
-   Ler primeiro
-   Leiame
-   Remover
-   Instalação
-   Suporte
-   What's New

A lista de programas a seguir não é fixável e são excluídos da lista usada com mais frequência.

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

As listas anteriores são armazenadas nos valores do Registro a seguir.

> [!Note]  
> Essas listas não devem ser modificadas por aplicativos. Use um dos métodos de lista de exclusão listados anteriormente para a mesma experiência.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)
</dt> <dt>

[**GetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid)
</dt> <dt>

[Extensões da barra de tarefas](taskbar-extensions.md)
</dt> <dt>

[**ICustomDestinationList::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[**IApplicationDocumentLists::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[**IApplicationDestinations::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
