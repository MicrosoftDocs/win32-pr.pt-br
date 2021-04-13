---
title: Criando um aplicativo de faixa de faixas
description: A estrutura da faixa de opção do Windows é composta por duas plataformas de desenvolvimento diferentes, mas dependentes, uma linguagem de marcação baseada em linguagem XAML (XAML) para declarar controles e seu layout visual, e um conjunto de interfaces com base em C++ Component Object Model (COM) para definir a funcionalidade de comando e os ganchos de aplicativos. Essa divisão de trabalho dentro da arquitetura da estrutura da faixa de Ribbon exige que um desenvolvedor que queira aproveitar os recursos avançados da interface do usuário oferecidos pela estrutura deve criar e descrever a interface do usuário em marcação e, em seguida, usar as interfaces de COM do Framework da faixa de faixas para conectar a estrutura ao aplicativo host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Faixa de-se do Windows, criando aplicativos
- Faixa de faixas, criando aplicativos
- Faixa de mapa do Windows, roteiro
- Faixa de mapa, roteiro
- Faixa de medida do Windows, marcação
- Faixa de, marcação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366437"
---
# <a name="creating-a-ribbon-application"></a>Criando um aplicativo de faixa de faixas

A estrutura da faixa de opção do Windows é composta por duas plataformas de desenvolvimento diferentes, mas dependentes: uma linguagem de marcação baseada em linguagem XAML (XAML) para declarar controles e seu layout visual, e um conjunto de interfaces baseado em C++ Component Object Model (COM) para definir a funcionalidade de comando e os ganchos de aplicativos. Essa divisão de trabalho dentro da arquitetura da estrutura da faixa de Ribbon exige que um desenvolvedor que queira aproveitar os recursos avançados da interface do usuário oferecidos pela estrutura deve criar e descrever a interface do usuário em marcação e, em seguida, usar as interfaces de COM do Framework da faixa de faixas para conectar a estrutura ao aplicativo host.

-   [Roteiro da faixa de medida](#ribbon-roadmap)
-   [Gravar a marcação](#write-the-markup)
    -   [Compilar a marcação](#compile-the-markup)
-   [Compilar o aplicativo](#build-the-application)
    -   [Inicializar a faixa de faixas](#initialize-the-ribbon)
    -   [Vincular a marcação ao aplicativo](#link-the-markup-to-the-application)
    -   [Compilar o aplicativo](#link-the-markup-to-the-application)
-   [Atualizações e execuções de tempo de execução](#run-time-updates-and-executions)
-   [Suporte a OLE](#ole-support)
-   [Tópicos relacionados](#related-topics)

## <a name="ribbon-roadmap"></a>Roteiro da faixa de medida

Os aspectos visuais de um aplicativo da faixa de faixas, como quais controles são exibidos e onde eles são colocados, são declarados na marcação (consulte [declarando comandos e controles com marcação da faixa de faixas](windowsribbon-schema.md)). A lógica do comando do aplicativo, como o que acontece quando um botão é pressionado, é implementada no código.

O processo de implementar uma faixa de quadro e incorporá-la em um aplicativo do Windows requer quatro tarefas básicas: escreva a marcação, Compile a marcação, grave o código e compile e vincule todo o aplicativo.

O diagrama a seguir ilustra o fluxo de trabalho para uma implementação de faixa de opções típica.

![diagrama mostrando o fluxo de trabalho para uma implementação de faixa de medida típica.](images/overviews/ribbonroadmap.png)

As seções a seguir descrevem esse processo mais detalhadamente.

## <a name="write-the-markup"></a>Gravar a marcação

Depois que a interface do usuário da faixa de Ribbon foi projetada, a primeira tarefa para um desenvolvedor de aplicativos é descrever a interface do usuário com a marcação da faixa de faixas.

> [!IMPORTANT]
> O arquivo de esquema de marcação de estrutura da faixa de Ribbon, UICC. xsd, é instalado com o Microsoft Windows Software Development Kit (SDK) para Windows 7 e .NET Framework 4,0. Usando o caminho de instalação padrão, o arquivo está localizado na pasta% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ \[ número da versão \] \\ bin, em que ele pode ser referenciado por muitos editores XML para fornecer dicas e preenchimento automático.

 

Controles de faixa de opção, comandos de faixa de opção (os elementos independentes de controle que fornecem a funcionalidade base para controles de faixa de forma) e todos os layouts de controle e relações visuais são declarados na marcação. A estrutura da marcação da faixa de visão enfatiza a distinção entre controles de faixa de vista e comandos por meio de duas hierarquias de nó primário: uma árvore de [comandos e recursos](windowsribbon-reference-elements-command.md) e uma árvore de [modos de exibição](windowsribbon-reference-elements-view.md) .

Todos os contêineres e ações que são expostos pela faixa de faixas são declarados na árvore de [comandos e recursos](windowsribbon-reference-elements-command.md) . Cada elemento de comando é associado a um conjunto de recursos, conforme exigido pelo design da interface do usuário.

Depois de criar os comandos para um aplicativo, você declara os controles na árvore [views](windowsribbon-reference-elements-view.md) e associa cada controle a um comando para expor a funcionalidade do comando. A estrutura da faixa de das faixas determina o posicionamento real dos controles com base na hierarquia de controle declarada aqui.

O exemplo de código a seguir ilustra como declarar um controle de botão, rotulado como sair do aplicativo e associá-lo a um comando de saída.


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> Embora seja possível usar qualquer extensão de nome de arquivo para o arquivo de marcação da faixa de faixas, o. xml é a extensão recomendada usada em toda a documentação.

 

### <a name="compile-the-markup"></a>Compilar a marcação

Depois que o arquivo de marcação da faixa de faixas é criado, ele deve ser compilado em um formato binário pelo compilador de marcação da faixa de forma, UICC (compilador de comando da interface do usuário), incluído no Windows Software Development Kit (SDK). Uma referência a esse arquivo binário é passada para o método [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante a inicialização da estrutura da faixa de faixas pelo aplicativo host.

UICC pode ser executado diretamente de uma janela de linha de comando ou adicionado como uma "etapa de compilação personalizada" no Visual Studio.

A imagem a seguir mostra o compilador de marcação UICC na janela shell CMD do SDK do Windows 7.

![captura de tela mostrando uicc.exe em uma janela de linha de comando.](images/overviews/screenshot-intentcl-commandline.png)

A imagem a seguir mostra o UICC adicionado como uma etapa de compilação personalizada no Visual Studio.

![captura de tela mostrando uicc.exe adicionado como uma etapa de compilação personalizada no Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

O UICC gera três arquivos: uma versão binária da marcação (. BML), um cabeçalho de definição de ID (arquivo. h) para expor elementos de marcação ao aplicativo host da faixa de bits e um [script de definição de recurso](../menurc/about-resource-files.md) (arquivo. rc) para vincular a imagem da faixa de bits e recursos de cadeia de caracteres ao aplicativo host no momento da compilação.

Para obter mais detalhes sobre a compilação da marcação da estrutura da faixa de faixas, consulte [compilando marcação da faixa](windowsribbon-intentcl.md)de

## <a name="build-the-application"></a>Compilar o aplicativo

Depois que a interface do usuário preliminar de um aplicativo de faixa de faixas foi projetada e implementada na marcação, o código do aplicativo deve ser escrito que inicializa a estrutura, consome a marcação e associa os comandos declarados na marcação aos manipuladores de comandos apropriados no aplicativo.

> [!IMPORTANT]
>
> Como a estrutura da faixa de bits é baseada em COM, é recomendável que os projetos de faixa de bits usem o \_ \_ operador uuidof () para referenciar os GUIDs para as interfaces de estrutura da faixa de referência (IIDs). Nesses casos em que não é possível usar o \_ \_ operador uuidof (), como quando um compilador não Microsoft é usado ou o aplicativo host é baseado em C, o IIDs deve ser definido pelo aplicativo, pois eles não estão contidos em UUID. lib.
>
> Se o IIDs for definido pelo aplicativo, os GUIDs especificados em UIRibbon. idl deverão ser usados.
>
> O UIRibbon. idl é fornecido como parte do [SDK (Software Development Kit) do Windows](https://msdn.microsoft.com/windows/bb980924.aspx) e pode ser encontrado no caminho de instalação padrão de% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ include.

 

### <a name="initialize-the-ribbon"></a>Inicializar a faixa de faixas

O diagrama a seguir ilustra as etapas necessárias para implementar um aplicativo de faixa de opções simples.

![diagrama mostrando as etapas necessárias para implementar uma implementação de faixa de faixas simples.](images/overviews/initializationsteps.png)

As etapas a seguir descrevem detalhadamente como implementar um aplicativo de faixa de opções simples.

1.  CoCreateInstance

    O aplicativo chama a função COM CoCreateInstance padrão com a ID de classe da estrutura da faixa de faixas para obter um ponteiro para a estrutura.

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  Initialize (HWND, IUIApplication \* )

    O aplicativo chama [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passando dois parâmetros: o identificador para a janela de nível superior que conterá a faixa de faixas e um ponteiro para a implementação de [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que permite que a estrutura faça retornos de chamada para o aplicativo.

    > \[! Fundamental\]  
    > A estrutura da faixa de faixas é inicializada como um STA (single-threaded apartment).

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI (instância, resourceName)

    O aplicativo chama [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para associar o recurso de marcação. O primeiro parâmetro dessa função é um identificador para a instância do aplicativo da faixa de faixas. O segundo parâmetro é o nome do recurso de marcação binária que foi compilado anteriormente. Ao passar a marcação binária para a estrutura da faixa de faixas, o aplicativo sinaliza o que a estrutura da faixa de faixas deve ser e como os controles devem ser organizados. Ele também fornece a estrutura com um manifesto de comandos para expor (como colar, recortar, localizar), que são usados pela estrutura quando ele faz retornos de chamada relacionados a comandos em tempo de execução.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  Retornos de chamada [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

    Após a conclusão das etapas 1 a 3, a estrutura da faixa de faixas sabe quais comandos serão expostos na faixa de faixas. No entanto, a estrutura ainda precisa de duas coisas antes que a faixa de opções seja totalmente funcional: uma maneira de informar ao aplicativo quando comandos são executados e uma maneira de obter recursos de comando, ou propriedades, em tempo de execução. Por exemplo, se uma caixa de combinação for exibida na interface do usuário, a estrutura precisará solicitar os itens com os quais preencher a caixa de combinação.

    Essas duas partes de funcionalidade são manipuladas por meio da interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) . Especificamente, para cada comando declarado na marcação binária (consulte a etapa 3 acima), a estrutura chama [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) para solicitar ao aplicativo um objeto **IUICommandHandler** para esse comando

    > [!Note]  
    > A interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) permite que um manipulador de comando seja associado a um ou mais comandos.

     

No mínimo, o aplicativo é necessário para implementar stubs de métodos [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que retornam E \_ NOTIMPL, conforme mostrado no exemplo a seguir.


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a>Vincular a marcação ao aplicativo

Neste ponto, os arquivos de recursos de marcação devem ser vinculados ao aplicativo host, incluindo uma referência ao arquivo de definição de recurso de marcação (que contém uma referência ao arquivo de cabeçalho de marcação) no arquivo de recurso de aplicativo. Por exemplo, um aplicativo chamado RibbonApp com um arquivo de recurso chamado ribbonUI. rc requer a seguinte linha no arquivo RibbonApp. rc.


```C++
#include "ribbonUI.rc"
```



Dependendo do compilador e do vinculador que está sendo usado, o script de definição de recurso também pode exigir compilação antes que o aplicativo da faixa de faixas possa ser compilado. A ferramenta de linha de comando do [compilador de recursos (RC)](../menurc/using-rc-the-rc-command-line-.md) fornecida com Microsoft Visual Studio e a SDK do Windows pode ser usada para essa tarefa.

### <a name="compile-the-application"></a>Compilar o aplicativo

Depois que o aplicativo da faixa de faixas é compilado, ele pode ser executado e a interface do usuário é testada. Se a interface do usuário exigir ajuste e não houver nenhuma alteração em nenhum manipulador de comando associado no código do aplicativo principal, revise o arquivo de origem da marcação, recompile a marcação com UICC.exe e vincule os novos arquivos de recurso de marcação. Quando o aplicativo é reiniciado, a interface do usuário modificada é exibida.

Tudo isso é possível sem tocar no código do aplicativo principal – uma melhoria significativa em relação ao desenvolvimento e à distribuição de aplicativos padrão.

## <a name="run-time-updates-and-executions"></a>Atualizações e execuções de tempo de execução

A estrutura de comunicação de tempo de execução da estrutura da faixa de opção baseia-se em um modelo de chamada push e pull, ou um chamador bidirecional.

Esse modelo permite que a estrutura informe o aplicativo quando um comando é executado e permite que a estrutura e o aplicativo consultem, atualizem e invalidam valores de propriedade e recursos de faixa de opções. Essa funcionalidade é fornecida por meio de várias interfaces e métodos.

A estrutura extrai informações de propriedade atualizadas do aplicativo da faixa de faixas por meio do método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) . Uma ID de comando e uma chave de propriedade, que identifica a propriedade de comando a ser atualizada, são passadas para o método que, em seguida, retorna ou envia um valor para essa chave de propriedade para a estrutura.

A estrutura chama [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando um comando é executado, identificando a ID de comando e o tipo de execução que ocorreu ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)). É aí que o aplicativo especifica a lógica de execução para um comando.

O diagrama a seguir ilustra a comunicação em tempo de execução para a execução do comando entre a estrutura e o aplicativo.

![diagrama que mostra um exemplo da comunicação de tempo de execução entre a estrutura da faixa de bits e um aplicativo host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> A implementação das funções [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) e [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) não é necessária para exibir inicialmente uma faixa de faixas em um aplicativo. No entanto, esses métodos são necessários para garantir que o aplicativo funcione corretamente quando comandos são executados pelo usuário.

 

## <a name="ole-support"></a>Suporte a OLE

Um aplicativo de faixa de faixas pode ser configurado como um servidor OLE para dar suporte à ativação de OLE fora do local.

Os objetos criados em um aplicativo de servidor OLE mantêm sua associação com o aplicativo de servidor quando inseridos (colados ou posicionados) em um aplicativo cliente OLE (ou contêiner). Em ativação de OLE fora do local, clicar duas vezes no objeto no aplicativo cliente abre uma instância dedicada do aplicativo de servidor e carrega o objeto para edição. Quando o aplicativo do servidor é fechado, todas as alterações feitas no objeto são refletidas no aplicativo cliente.

> [!Note]  
> A estrutura da faixa de bits não dá suporte à ativação de OLE in-loco. Os objetos criados em um servidor OLE baseado em faixa de bits não podem ser editados de dentro do aplicativo cliente OLE. Uma instância dedicada externa do aplicativo de servidor é necessária.


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declarando comandos e controles com marcação de faixa de medida](./windowsribbon-schema.md)
</dt> <dt>

[Diretrizes de experiência do usuário da faixa de das](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo de design da faixa de das](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




