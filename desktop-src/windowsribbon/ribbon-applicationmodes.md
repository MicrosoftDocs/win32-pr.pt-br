---
title: Reconfiguração da faixa de modo com modos de aplicativo
description: A estrutura da faixa de referência do Windows dá suporte à reconfiguração dinâmica e à exposição de elementos principais da interface do usuário da faixa de referência em tempo de execução, com base no estado do aplicativo (também conhecido como contexto).
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Faixa de-se do Windows, reconfigurando com modos de aplicativo
- Faixa de faixas, reconfigurando com modos de aplicativo
- reconfiguração da faixa de introdução do Windows com modos de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366031"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a>Reconfiguração da faixa de modo com modos de aplicativo

A estrutura da faixa de referência do Windows dá suporte à reconfiguração dinâmica e à exposição de elementos principais da interface do usuário da faixa de referência em tempo de execução, com base no estado do aplicativo (também conhecido como contexto). Declarados e associados a elementos específicos na marcação, os vários Estados com suporte de um aplicativo são chamados de modos de aplicativo.

-   [Introdução](#introduction)
-   [Interface do usuário contextual](#contextual-user-interface)
    -   [Um cenário de modo de aplicativo simples](#a-simple-application-mode-scenario)
-   [Implementando modos de aplicativo](#implementing-application-modes)
    -   [Identificar os modos](#identify-the-modes)
    -   [Atribuir controles aos modos de aplicativo](#assign-controls-to-application-modes)
    -   [Alternar modos em tempo de execução](#switch-modes-at-runtime)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Os modos de aplicativo consistem em grupos lógicos de controles que expõem alguma funcionalidade de aplicativo principal na interface do usuário da faixa de da Ribbon. Esses modos são habilitados ou desabilitados dinamicamente pelo aplicativo por meio de uma chamada para o método de estrutura [**IUIFramework:: Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes), o que ativa ou desativa a visibilidade de um ou mais modos de aplicativo.

## <a name="contextual-user-interface"></a>Interface do usuário contextual

A estrutura da faixa de faixas fornece uma experiência de usuário avançada incorporando controles dinâmicos que respondem diretamente à interação do usuário e ao contexto do aplicativo. Essa interface do usuário contextual rica é fornecida por meio de uma combinação dos seguintes mecanismos:

-   Galerias – controles baseados em coleção que dão suporte à manipulação dinâmica de suas coleções de itens.
-   Guias contextuais – guias da faixa de opção que têm sua visibilidade determinada por uma alteração no contexto do espaço de trabalho, como a seleção de uma imagem em um documento.
-   Modos de aplicativo-funcionalidade de aplicativo principal que depende do contexto do aplicativo.

Em alguns aspectos, os modos de aplicativo aparecem funcionalmente semelhantes às guias contextuais. No entanto, a distinção fundamental está na intenção e no escopo de cada uma.

Os controles contextuais são ativados em resposta a uma alteração de contexto dentro de um aplicativo. Por exemplo, no Microsoft Paint para Windows 7, uma guia contextual que contém grupos de comandos relacionados a texto é exibida quando um usuário insere uma área de texto no espaço de trabalho. Essa guia contextual não contém comandos de núcleo para o aplicativo e é exposta apenas na interface do usuário porque o contexto *dentro* do aplicativo foi alterado. A funcionalidade principal do aplicativo (os comandos de edição de imagem) ainda é relevante e está disponível para o usuário, mesmo com a guia contextual visível.

Os modos de aplicativo diferem dos controles contextuais no que reconfiguram a funcionalidade em resposta a alterações no contexto em que o aplicativo está operando. Os modos de aplicativo ficam em um nível mais alto de abstração; Eles fornecem uma maneira de reconfigurar a funcionalidade básica de um aplicativo em vez de expor temporariamente a funcionalidade que não é um componente principal da interface do usuário. Por exemplo, no Microsoft Paint para Windows 7, uma opção no modo de aplicativo ocorre quando o comando **Visualizar impressão** é invocado. Quando o Microsoft Paint alterna para o modo de **visualização de impressão**, o contexto no qual o aplicativo está operando muda de editar para visualização. Como resultado, a funcionalidade principal do aplicativo é alterada até que a **visualização de impressão** seja cancelada e o aplicativo Insira o contexto de edição novamente.

### <a name="a-simple-application-mode-scenario"></a>Um cenário de modo de aplicativo simples

O cenário a seguir demonstra como os modos de aplicativo são usados, em um aplicativo chamado RibbonApp, para expor aspectos discretos da funcionalidade básica.

Dois modos de aplicativo são definidos em RibbonApp:

-   O modo **simples** expõe comandos básicos em toda a interface do usuário da faixa de faixas. Esses comandos aparecem em todos os momentos, não importa qual modo de aplicativo está ativo.
-   O modo **avançado** expõe comandos complexos destinados a usuários especialistas do aplicativo. Esses comandos avançados aparecem em toda a interface do usuário da faixa de, além dos comandos simples.

Por padrão, RibbonApp é definido para abrir no modo **simples** e os comandos necessários para usuários iniciantes são exibidos no **menu aplicativo** e na guia **página inicial** . As capturas de tela a seguir mostram o **menu do aplicativo** RibbonApp e a guia **página inicial** no modo **simples** , destacando os controles modais.

![captura de tela mostrando uma guia para o modo de aplicativo simples.](images/overviews/appmode-hometab.png)![captura de tela mostrando o menu do aplicativo para o modo de aplicativo simples.](images/overviews/appmode-simpleappmenu.png)

Embora esses comandos possam ser suficientes para usuários iniciantes, o RibbonApp também dá suporte a usuários especialistas por meio de um modo **avançado** que, quando ativado, clicando no botão **alternar para o modo avançado** no **menu aplicativo**, exibe funcionalidade básica adicional.

Esse cenário é facilmente implementado pela Associação de vários elementos na marcação a modos de aplicativo discretos que podem ser ativados e desativados conforme necessário. As capturas de tela a seguir mostram o **menu do aplicativo** RibbonApp e a guia **página inicial** no modo **avançado** , destacando os controles modais.

![captura de tela mostrando uma guia para o modo de aplicativo avançado.](images/overviews/appmode-advancedtab.png)![captura de tela mostrando o menu do aplicativo para o modo de aplicativo avançado.](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a>Implementando modos de aplicativo

Esta seção descreve as três etapas normalmente necessárias para a implementação dos modos de aplicativo da estrutura da faixa de faixas. RibbonApp é usado para fornecer um exemplo para cada etapa.

### <a name="identify-the-modes"></a>Identificar os modos

Cada modo em um aplicativo deve representar um conjunto lógico de funcionalidade que depende do contexto em que um aplicativo é capaz de operar. Por exemplo, se um aplicativo exibe controles que são relevantes apenas quando uma conexão de rede é detectada, esses controles operam dentro de um contexto de rede que pode justificar a criação de um modo de **rede** .

RibbonApp tem dois contextos que podem estar ativos em um determinado momento: **simples** e **avançado**. Portanto, RibbonApp exige dois modos: **simples** e **avançado**.

### <a name="assign-controls-to-application-modes"></a>Atribuir controles aos modos de aplicativo

Depois que os modos de aplicativo forem identificados, atribua cada controle de faixa de faixas a um modo declarando um atributo *ApplicationModes* na marcação para os elementos de controle que dão suporte aos modos de aplicativo.

A exibição da faixa de opções permite que os modos sejam especificados nos seguintes elementos de controle:

-   Elementos da [**guia**](windowsribbon-element-tab.md) de núcleo.
-   [**Agrupar**](windowsribbon-element-group.md) elementos que são elementos filho de um elemento de [**guia**](windowsribbon-element-tab.md) de núcleo.
-   Elementos [**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)e [**DropDownButton**](windowsribbon-element-dropdownbutton.md) atribuídos a um [**menu de menus**](windowsribbon-element-menugroup.md) no menu do [aplicativo](windowsribbon-controls-applicationmenu.md).
    > [!Note]  
    > Os elementos [**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)e [**DropDownButton**](windowsribbon-element-dropdownbutton.md) não podem ser atribuídos a um modo, a menos que hospedados no [menu do aplicativo](windowsribbon-controls-applicationmenu.md).

     

No Framework da faixa de faixas, esses elementos de controle são chamados de controles modais. Eles aparecerão apenas se um modo ao qual estão associados estiver ativo na interface do usuário.

Elementos de controle que estão contidos em um controle modal herdam o comportamento do modo de aplicativo. Por exemplo, se um controle modal de [**grupo**](windowsribbon-element-group.md) for atribuído a um modo **avançado** e o modo **avançado** não estiver ativo, esse **grupo** e todos os controles nela, modal ou não, não estarão visíveis na interface do usuário da faixa de Ribbon.

Com o uso do atributo *ApplicationModes* , os modos são atribuídos a controles modais em uma relação 1: N (um-para-muitos), em que um único controle modal pode ser associado a vários modos.

A estrutura da faixa de referência refere-se aos modos numericamente, de 0 a 31, com o modo 0 considerado o modo padrão que é ativado automaticamente quando um aplicativo da faixa de faixas é iniciado. Qualquer controle modal que não especifique um atributo *ApplicationModes* é considerado como membro do modo padrão.

No RibbonApp, **simples** é o modo padrão, com a funcionalidade de modo **avançado** exibida somente quando é iniciado pelo usuário.

O exemplo a seguir demonstra a marcação necessária para RibbonApp.


```C++
<Application.Views>
  <Ribbon>

    <!--Application Menu-->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName='cmdAppMenu'>                    
        <MenuGroup>
          <Button CommandName='cmdSave'/>                        
          <Button CommandName='cmdExportMetadata' ApplicationModes='1'/>                   
        </MenuGroup>              
        <MenuGroup>
          <Button CommandName='cmdSwitchModes' ApplicationModes ='0,1'/>
          <Button CommandName='cmdExit'/>
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
            
    <!--Tabs-->
    <Ribbon.Tabs>
      <!--Home Tab-->
      <Tab CommandName='cmdHomeTab'>
                    
        <!--Scaling Policy for Home tab-->
        <Tab.ScalingPolicy>
          <ScalingPolicy>
            <ScalingPolicy.IdealSizes>
              <Scale Group='cmdSimpleControlsGroup' Size='Medium'/>                                
            </ScalingPolicy.IdealSizes>                     
          </ScalingPolicy>
        </Tab.ScalingPolicy>     
                    
        <!--Simple Controls Group-->
        <Group CommandName='cmdSimpleControlsGroup' SizeDefinition='ThreeButtons-OneBigAndTwoSmall'>                        
          <Button CommandName="cmdPaste" />
          <Button CommandName='cmdCut'/>                        
          <Button CommandName='cmdCopy'/>                        
        </Group>
      </Tab>
                
      <!--Advanced Tab-->
      <Tab CommandName='cmdAdvancedTab' ApplicationModes='1'>
        <!--Advanced Controls Group-->
        <Group CommandName='cmdMetadataGroup' ApplicationModes='1' SizeDefinition='TwoButtons'>
          <Button CommandName='cmdEditMetadata' />
          <Button CommandName='cmdCheckErrors' />
        </Group>
      </Tab>
    </Ribbon.Tabs>                   
                             
  </Ribbon>         
</Application.Views>
```



Este exemplo demonstra o seguinte:

-   O modo padrão 0 não precisa ser declarado explicitamente. Como os controles modais que não especificam o atributo *ApplicationModes* são associados automaticamente ao modo 0 (modo **simples** no exemplo RibbonApp), não é necessário declarar explicitamente o atributo para controles modais padrão.
-   Os controles podem ser associados a vários modos. Para RibbonApp, a única necessidade do atributo *ApplicationModes* em um controle de modo **simples** é o `cmdSwitchModes` botão, pois ele faz parte dos modos **simples** e **avançado** . Se um dos modos estiver ativo, esse controle aparecerá no [menu do aplicativo](windowsribbon-controls-applicationmenu.md).
-   Os controles modais não herdam de seus pais. A guia **avançado** de RibbonApp contém um grupo de **metadados** ; ambos os controles modais são atribuídos ao modo 1 (modo **avançado** ). A atribuição da guia **avançado** ao modo 1 não atribui automaticamente controles filho, como o grupo de **metadados** , ao modo 1. Isso permite que qualquer grupo dentro de uma guia seja habilitado ou desabilitado independentemente em tempo de execução.
-   Os controles não modais ainda podem depender de opções de modo. Os botões **Editar metadados** e **verificar erros** de RibbonApp são para usuários avançados e estão disponíveis somente quando o usuário alterna para o modo **avançado** . Controles de botão que não são hospedados dentro do [menu do aplicativo](windowsribbon-controls-applicationmenu.md) não são modais; no entanto, como esses botões são hospedados dentro de um controle modal (o grupo de **metadados** ), eles ficam visíveis quando o grupo está visível. Portanto, esses botões são exibidos quando o modo avançado é ativado e o grupo de **metadados** é exposto na interface do usuário da faixa de faixas.

### <a name="switch-modes-at-runtime"></a>Alternar modos em tempo de execução

Depois que os modos são definidos na marcação, eles podem ser facilmente habilitados ou desabilitados em resposta a eventos contextuais. Conforme mencionado anteriormente, os aplicativos da faixa de faixas sempre começam no modo padrão 0. Depois que o aplicativo for inicializado e o modo 0 estiver ativo, o conjunto de modos ativos poderá ser alterado chamando a função [**IUIFramework:: Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) . Essa função usa um inteiro de 32 bits como uma representação bit a bit dos modos que devem estar ativos; o bit menos significativo representa o modo 0 e o bit mais significativo representa o modo 31. Se um bit for definido como zero, o modo não estará ativo na interface do usuário da faixa de bits.

No RibbonApp, quando um usuário habilita o modo **avançado** , os comandos avançados são exibidos junto com os comandos simples. O manipulador de comandos do botão **alternar para o modo avançado** chama [**IUIFramework:: setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) para definir os modos 0 (**simples**) e 1 (**avançado**) como ativos na interface do usuário. O exemplo a seguir é o código RibbonApp para essa chamada de função:


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> A macro MAKEAPPMODE do Framework da faixa de opção \_ simplifica a tarefa de definir esses bits corretamente em preparação para a chamada para [**IUIFramework:: setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).

 

Este exemplo demonstra o seguinte:

-   Use a macro MAKEAPPMODE da interface do usuário \_ para criar um conjunto de modos.
-   Os modos são definidos explicitamente e atomicamente. O valor inteiro que é passado para [**IUIFramework:: Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) representa os modos que estarão ativos após o retorno da função. Embora o modo **simples** tenha sido anteriormente ativo, **IUIFramework:: setmodes** deve indicar que o modo **simples** permanece ativo quando o modo **avançado** é ativado.
-   O modo padrão pode ser removido. Embora no RibbonApp o modo padrão (modo 0) nunca seja removido, ele pode ser removido com a seguinte chamada: `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` , expondo somente os comandos avançados na interface do usuário.

> [!Note]  
> Quando os modos de um aplicativo são reconfigurados, a faixa de faixas tentará preservar a guia selecionada anteriormente na interface do usuário. Se o novo conjunto de modos não contiver mais a guia que foi selecionada antes da chamada, a faixa de opções selecionará a guia em seu layout mais próximo ao [menu do aplicativo](windowsribbon-controls-applicationmenu.md). Essa guia deve conter os comandos que são mais relevantes para o usuário. Para obter mais informações, consulte [diretrizes de experiência do usuário da faixa](https://msdn.microsoft.com/library/cc872782.aspx)de das.

 

## <a name="remarks"></a>Comentários

A faixa de faixas deve ter pelo menos um modo ativo em todos os momentos. Se um aplicativo tentar desativar todos os modos chamando [**IUIFramework:: Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) com um valor de modo de 0, e \_ a falha será retornada e o conjunto de modos ativo permanecerá inalterado.

A estrutura requer que, pelo menos, uma guia exista na interface do usuário da faixa de de todas as ocasiões. Como resultado, deve haver pelo menos uma guia exposta pelo modo padrão (modo 0) e depois de cada opção de modo.

Nem todas as áreas da interface do usuário da faixa de lista são afetadas pelos modos de aplicativo. Por exemplo, se a desabilitação de um modo causar o desaparecimento dos botões da faixa de faixas que foram adicionados anteriormente à [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md), esses botões permanecerão na barra de ferramentas de acesso rápido, permitindo que os usuários executem os comandos ligados aos botões. Como regra geral, se um comando pertencer a um ou mais modos inativos, esse comando também deverá ser desabilitado definindo a [propriedade \_ PKEY \_ habilitada da interface do usuário](windowsribbon-reference-properties-uipkey-enabled.md) como 0 (variante \_ false).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes de experiência do usuário da faixa de das](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Exibindo guias contextuais](ribbon-contextualtabs.md)
</dt> </dl>

 

 