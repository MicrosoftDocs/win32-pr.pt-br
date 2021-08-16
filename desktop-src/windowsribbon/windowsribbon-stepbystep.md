---
title: Criando um aplicativo de faixa de opções
description: A estrutura de Faixa de Opções do Windows é composta por duas plataformas de desenvolvimento distintas, mas dependentes, uma linguagem de marcação baseada em Extensible Application Markup Language (XAML) para declarar controles e seu layout visual e um conjunto de interfaces baseado em COM (C++ Component Object Model) para definir a funcionalidade de comando e os ganchos de aplicativo. Essa divisão de mão de obra na arquitetura da estrutura da Faixa de Opções requer que um desenvolvedor que deseja aproveitar os recursos avançados de interface do usuário oferecidos pela estrutura deve projetar e descrever a interface do usuário na marcação e, em seguida, usar as interfaces COM da estrutura de faixa de opções para conectar a estrutura ao aplicativo host.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Windows Faixa de opções, criando aplicativos
- Faixa de opções, criando aplicativos
- Windows Faixa de opções, roteiro
- Faixa de opções, roteiro
- Windows Faixa de opções, marcação
- Faixa de opções, marcação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3cc3395b2fe53759152f5d0244c6546c08832bda190035a918af6049a99811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849975"
---
# <a name="creating-a-ribbon-application"></a>Criando um aplicativo de faixa de opções

A estrutura de Faixa de Opções do Windows é composta por duas plataformas de desenvolvimento distintas, mas dependentes: uma linguagem de marcação baseada em Extensible Application Markup Language (XAML) para declarar controles e seu layout visual e um conjunto baseado em COM (C++ Component Object Model) de interfaces para definir a funcionalidade de comando e ganchos de aplicativo. Essa divisão de mão de obra na arquitetura da estrutura da Faixa de Opções requer que um desenvolvedor que deseja aproveitar os recursos avançados de interface do usuário oferecidos pela estrutura deve projetar e descrever a interface do usuário na marcação e, em seguida, usar as interfaces COM da estrutura de faixa de opções para conectar a estrutura ao aplicativo host.

-   [Roteiro da Faixa de Opções](#ribbon-roadmap)
-   [Gravar a marcação](#write-the-markup)
    -   [Compilar a marcação](#compile-the-markup)
-   [Criar o aplicativo](#build-the-application)
    -   [Inicializar a faixa de opções](#initialize-the-ribbon)
    -   [Vincular a marcação ao aplicativo](#link-the-markup-to-the-application)
    -   [Compilar o aplicativo](#link-the-markup-to-the-application)
-   [Execuções e atualizações de tempo de execução](#run-time-updates-and-executions)
-   [Suporte ao OLE](#ole-support)
-   [Tópicos relacionados](#related-topics)

## <a name="ribbon-roadmap"></a>Roteiro da Faixa de Opções

Os aspectos visuais de um aplicativo de Faixa de Opções, como quais controles são exibidos e onde são colocados, são declarados na marcação (consulte Declarando comandos e controles com marcação de faixa de [opções).](windowsribbon-schema.md) A lógica de comando do aplicativo, como o que acontece quando um botão é pressionado, é implementada no código.

O processo de implementar uma Faixa de Opções e incorporá-la em um aplicativo Windows requer quatro tarefas básicas: gravar a marcação, compilar a marcação, escrever o código e compilar e vincular todo o aplicativo.

O diagrama a seguir ilustra o fluxo de trabalho para uma implementação típica da Faixa de Opções.

![diagrama mostrando o fluxo de trabalho para uma implementação de faixa de opções típica.](images/overviews/ribbonroadmap.png)

As seções a seguir descrevem esse processo mais detalhadamente.

## <a name="write-the-markup"></a>Gravar a marcação

Depois que a interface do usuário da Faixa de Opções tiver sido projetada, a primeira tarefa para um desenvolvedor de aplicativos será descrever a interface do usuário com marcação de Faixa de Opções.

> [!IMPORTANT]
> O arquivo de esquema de marcação da estrutura ribbon, UICC.xsd, é instalado com o SDK (Software Development Kit) do Microsoft Windows para Windows 7 e .NET Framework 4.0. Usando o caminho de instalação padrão, o arquivo está localizado na pasta Bin %ProgramFiles% SDKs da Microsoft Windows de número de versão, na qual ele pode ser referenciado por muitos editores XML para fornecer dicas e preenchimento \\ \\ \\ \[ \] \\ automático.

 

Controles de faixa de opções, Comandos da Faixa de Opções (os elementos independentes de controle que fornecem a funcionalidade base para controles de Faixa de Opções) e todos os layouts de controle e relações visuais são declarados na marcação. A estrutura da marcação Faixa de Opções enfatiza a distinção entre controles de Faixa de Opções e Comandos por meio de duas hierarquias de nó primário: uma árvore [Comandos](windowsribbon-reference-elements-command.md) e Recursos e uma árvore [exibições.](windowsribbon-reference-elements-view.md)

Todos os contêineres e ações expostos pela Faixa de Opções são declarados na árvore [Comandos e](windowsribbon-reference-elements-command.md) Recursos. Cada elemento Command está associado a um conjunto de recursos, conforme exigido pelo design da interface do usuário.

Depois de criar os Comandos para um aplicativo, você declara controles na árvore [Exibições](windowsribbon-reference-elements-view.md) e vincula cada controle a um Comando para expor a funcionalidade Comando. A estrutura da Faixa de Opções determina o posicionamento real dos controles com base na hierarquia controle declarada aqui.

O exemplo de código a seguir ilustra como declarar um controle Button, rotulado Sair do aplicativo e associá-lo a um comando Exit.


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
> Embora seja possível usar qualquer extensão de nome de arquivo para o arquivo de marcação faixa de opções, .xml é a extensão recomendada usada em toda a documentação.

 

### <a name="compile-the-markup"></a>Compilar a marcação

Depois que o arquivo de marcação faixa de opções for criado, ele deverá ser compilado em um formato binário pelo compilador de marcação Ribbon, UICC (Compilador de Comando da Interface do Usuário), que está incluído no SDK (software development kit) do Windows. Uma referência a esse arquivo binário é passada para o método [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) durante a inicialização da estrutura ribbon pelo aplicativo host.

O UICC pode ser executado diretamente de uma janela de linha de comando ou adicionado como uma "Etapa de Build Personalizada" no Visual Studio.

A imagem a seguir mostra o compilador de marcação UICC na Windows shell do CMDK do SDK 7.

![captura de tela mostrando uicc.exe em uma janela de linha de comando.](images/overviews/screenshot-intentcl-commandline.png)

A imagem a seguir mostra o UICC adicionado como uma etapa de build personalizada no Visual Studio.

![captura de tela mostrando uicc.exe adicionado como uma etapa de build personalizada no Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

O UICC gera três arquivos: uma versão binária da marcação (.bml), um header de definição de ID (arquivo .h) para expor elementos de marcação ao aplicativo host da Faixa de Opções e um [script](../menurc/about-resource-files.md) de definição de recurso (arquivo .rc) para vincular recursos de imagem e cadeia de caracteres da Faixa de Opções ao aplicativo host no tempo de compilação.

Para obter mais detalhes sobre como compilar a marcação da estrutura da Faixa de Opções, consulte [Compilando marcação de faixa de opções.](windowsribbon-intentcl.md)

## <a name="build-the-application"></a>Compilar o aplicativo

Depois que a interface do usuário preliminar de um aplicativo de Faixa de Opções tiver sido projetada e implementada na marcação, o código do aplicativo deverá ser escrito que inicializa a estrutura, consumirá a marcação e vinculará os Comandos declarados na marcação aos manipuladores de comando apropriados no aplicativo.

> [!IMPORTANT]
>
> Como a estrutura da Faixa de Opções é baseada em COM, é recomendável que os projetos da Faixa de Opções usem o operador uuidof() para referenciar os GUIDs para interfaces de estrutura de faixa de opções \_ \_ (IIDs). Nesses casos em que não é possível usar o operador uuidof(), como quando um compilador não Microsoft é usado ou o aplicativo host é baseado em C, os IIDs devem ser definidos pelo aplicativo, pois eles não estão contidos em \_ \_ uuid.lib.
>
> Se os IIDs são definidos pelo aplicativo, os GUIDs especificados em UIRibbon.idl devem ser usados.
>
> UIRibbon.idl é fornecidas como parte do [SDK (Software Development Kit)](https://msdn.microsoft.com/windows/bb980924.aspx) do Windows e podem ser encontradas no caminho de instalação padrão de %ProgramFiles% \\ SDKs da Microsoft Windows \\ \\ v7.0 \\ Include.

 

### <a name="initialize-the-ribbon"></a>Inicializar a faixa de opções

O diagrama a seguir ilustra as etapas necessárias para implementar um aplicativo de Faixa de Opções simples.

![diagrama mostrando as etapas necessárias para implementar uma implementação de faixa de opções simples.](images/overviews/initializationsteps.png)

As etapas a seguir descrevem detalhadamente como implementar um aplicativo de Faixa de Opções simples.

1.  Cocreateinstance

    O aplicativo chama a função COM CoCreateInstance padrão com a ID da classe da estrutura ribbon para obter um ponteiro para a estrutura.

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

    

2.  Initialize(hwnd, IUIApplication \* )

    O aplicativo chama [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passando dois parâmetros: o handle para a janela de nível superior que conterá a Faixa de Opções e um ponteiro para a implementação [**de IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) que permite que a estrutura faça retornos de chamada para o aplicativo.

    > \[! Importante\]  
    > A estrutura da Faixa de Opções é inicializada como um STA (single-threaded apartment).

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI(instance, resourceName)

    O aplicativo chama [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) para vincular o recurso de marcação. O primeiro parâmetro dessa função é um handle para a instância do aplicativo Ribbon. O segundo parâmetro é o nome do recurso de marcação binária que foi compilado anteriormente. Ao passar a marcação binária para a estrutura ribbon, o aplicativo sinaliza o que a estrutura da Faixa de Opções deve ser e como os controles devem ser organizados. Ele também fornece à estrutura um manifesto de comandos a expor (como Colar, Recortar, Encontrar), que são usados pela estrutura quando ele faz retornos de chamada relacionados ao comando em tempo de operação.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  [**Retornos de chamada IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

    Depois que as etapas 1 a 3 são concluídas, a estrutura da Faixa de Opções sabe quais Comandos expor na Faixa de Opções. No entanto, a estrutura ainda precisa de duas coisas antes que a Faixa de Opções seja totalmente funcional: uma maneira de dizer ao aplicativo quando os comandos são executados e uma maneira de obter recursos de comando ou propriedades, em tempo de execução. Por exemplo, se uma caixa de combinação for exibida na interface do usuário, a estrutura precisará solicitar os itens com os quais preencher a caixa de combinação.

    Essas duas partes da funcionalidade são tratadas por meio da interface [**IUICommandHandler.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) Especificamente, para cada comando declarado na marcação binária (consulte a Etapa 3 acima), a estrutura chama [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) para solicitar ao aplicativo um objeto **IUICommandHandler** para esse comando

    > [!Note]  
    > A interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) permite que um manipulador de comandos seja vinculado a um ou mais Comandos.

     

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

Neste ponto, os arquivos de recurso de marcação devem ser vinculados ao aplicativo host, incluindo uma referência ao arquivo de definição de recurso de marcação (que contém uma referência ao arquivo de header de marcação) no arquivo de recurso do aplicativo. Por exemplo, um aplicativo chamado RibbonApp com um arquivo de recurso chamado ribbonUI.rc requer a seguinte linha no arquivo RibbonApp.rc.


```C++
#include "ribbonUI.rc"
```



Dependendo do compilador e do linker que está sendo usado, o script de definição de recurso também pode exigir a compilação antes que o aplicativo ribbon possa ser compilado. A ferramenta de linha de [comando rc (compilador](../menurc/using-rc-the-rc-command-line-.md) de recursos) que acompanha Microsoft Visual Studio e o SDK do Windows podem ser usados para essa tarefa.

### <a name="compile-the-application"></a>Compilar o aplicativo

Depois que o aplicativo Ribbon for compilado, ele poderá ser executado e a interface do usuário será testada. Se a interface do usuário exigir ajustes e não houver alterações em manipuladores de comando associados no código do aplicativo principal, revise o arquivo de origem de marcação, recompile a marcação com UICC.exe e vincule os novos arquivos de recurso de marcação. Quando o aplicativo é reiniciado, a interface do usuário modificada é exibida.

Tudo isso é possível sem tocar no código do aplicativo principal – uma melhoria significativa em relação ao desenvolvimento e à distribuição de aplicativos padrão.

## <a name="run-time-updates-and-executions"></a>Execuções e atualizações de tempo de execução

A estrutura de comunicação em tempo de run time da estrutura da Faixa de Opções baseia-se em um modelo de push e pull ou chamador de duas vias.

Esse modelo permite que a estrutura informe o aplicativo quando um Comando é executado e permite que a estrutura e o aplicativo consultem, atualizem e invalidem os valores de propriedade e os recursos da Faixa de Opções. Essa funcionalidade é fornecida por meio de várias interfaces e métodos.

A estrutura recebe informações de propriedade atualizadas do aplicativo Ribbon por meio do método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) Uma ID de comando e uma chave de propriedade, que identifica a propriedade Command a ser atualizada, são passadas para o método que retorna, ou e push, um valor para essa chave de propriedade para a estrutura.

A estrutura chama [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando um comando é executado, identificando a ID de comando e o tipo de execução que ocorreu ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)). É aqui que o aplicativo especifica a lógica de execução de um comando.

O diagrama a seguir ilustra a comunicação em tempo de execução para execução de comando entre a estrutura e o aplicativo.

![diagrama mostrando um exemplo da comunicação em tempo de run-time entre a estrutura da faixa de opções e um aplicativo host.](images/overviews/updatesandexecutions.png)

> [!Note]  
> A implementação das funções [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) e [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) não é necessária para exibir inicialmente uma Faixa de Opções em um aplicativo. No entanto, esses métodos são necessários para garantir que o aplicativo funcione corretamente quando os comandos são executados pelo usuário.

 

## <a name="ole-support"></a>Suporte ao OLE

Um aplicativo de Faixa de Opções pode ser configurado como um servidor OLE para dar suporte à ativação OLE fora do local.

Objetos criados em um aplicativo de servidor OLE mantêm sua associação com o aplicativo de servidor quando inseridos (colar ou colocados) em um aplicativo cliente OLE (ou contêiner). Na ativação OLE fora do local, clicar duas vezes no objeto no aplicativo cliente abre uma instância dedicada do aplicativo de servidor e carrega o objeto para edição. Quando o aplicativo de servidor é fechado, todas as alterações feitas no objeto são refletidas no aplicativo cliente.

> [!Note]  
> A estrutura da Faixa de Opções não dá suporte à ativação OLE in-place. Objetos criados em um servidor OLE baseado em Faixa de Opções não podem ser editados de dentro do aplicativo cliente OLE. Uma instância dedicada externa do aplicativo de servidor é necessária.


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Declarando comandos e controles com marcação de faixa de opções](./windowsribbon-schema.md)
</dt> <dt>

[Diretrizes de experiência do usuário da faixa de opções](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo de design da faixa de opções](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




