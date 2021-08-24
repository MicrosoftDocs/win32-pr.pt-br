---
description: a partir do Microsoft Windows XP Tablet pc Edition Software Development Kit (SDK) versão 1,0, o painel de entrada do Tablet pc no nível do sistema fornece um mecanismo universal para realizar a entrada de texto na plataforma Windows, embora não forneça acesso programático. O objeto Tablet PC SDK versão 1,5 PenInputPanel integra as ferramentas de entrada de texto em aplicativos.
ms.assetid: 14fe4963-ab9b-4c78-9f17-791c68378ef0
title: Sobre o painel de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044e8c3a43127bd765fd5004329352956e4be8bb9f214f8dda8896fa318832a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119844406"
---
# <a name="about-the-input-panel"></a>Sobre o painel de entrada

\[[**PenInputPanel**](peninputpanel-class.md) foi substituído por [**TextInput**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel). Para obter mais informações, consulte [programando o painel de entrada de texto](programming-the-text-input-panel.md).\]

a partir do Microsoft Windows XP Tablet pc Edition Software Development Kit (SDK) versão 1,0, o painel de entrada do Tablet pc no nível do sistema fornece um mecanismo universal para realizar a entrada de texto na plataforma Windows, embora não forneça acesso programático. O objeto Tablet PC SDK versão 1,5 [**PenInputPanel**](peninputpanel-class.md) integra as ferramentas de entrada de texto em aplicativos.

O gráfico a seguir mostra o painel de entrada da caneta exibido sobre a amostra de [exemplo de formulário de declarações automática](auto-claims-form-sample.md) .

![painel de entrada da caneta exibido sobre exemplo de formulário de declarações automáticas](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

O objeto [**PenInputPanel**](peninputpanel-class.md) é conveniente para os desenvolvedores de aplicativos. Não é necessário substituir controles em formulários existentes. Você pode simplesmente anexar objetos **PenInputPanel** a controles existentes que recebem entrada de texto, e eles podem começar a receber entrada do objeto **PenInputPanel** .

O objeto [**PenInputPanel**](peninputpanel-class.md) adota as configurações do painel de entrada para as seguintes propriedades:

-   Layout
-   Espessura da tinta
-   Tempo limite de reconhecimento
-   Tamanho da caixa, modo de envio e outras configurações específicas para entrada em caixas do leste asiático

O objeto [**PenInputPanel**](peninputpanel-class.md) não fornece acesso à tinta subjacente. Para obter a tinta, use o controle [InkPicture](inkpicture-control-reference.md) .

O objeto [**PenInputPanel**](peninputpanel-class.md) fornece uma interface do usuário (IU) in-loco que é facilmente detectável pelos usuários finais de seus aplicativos. Ele é ativado automaticamente quando o usuário toca em uma janela com um objeto **PenInputPanel** usando a caneta eletrônica. O painel de entrada da caneta é exibido automaticamente quando o sistema detecta um evento CursorButtonUp para a janela à qual o objeto **PenInputPanel** está anexado. A ativação automática pode ser desabilitada definindo a propriedade [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) como **false**.

O painel de entrada da caneta não aparece automaticamente em eventos do mouse. Os eventos de caneta são convertidos em eventos de mouse ao usar os serviços de terminal. O objeto [**PenInputPanel**](peninputpanel-class.md) não funciona em uma conexão de serviços de terminal.

## <a name="pen-input-panel-input-modes"></a>Modos de entrada do painel de entrada da caneta

O objeto [**PenInputPanel**](peninputpanel-class.md) permite a funcionalidade do teclado ou a entrada de manuscrito, com teclados adicionais para auxiliar a entrada. A interface do usuário para o painel de entrada da caneta inclui:

-   Painel de escrita
-   Teclado de escrita para idiomas do leste asiático
-   Teclados de QuickKeys
-   Teclado in-loco

A disponibilidade do painel de escrita versus o teclado de escrita para idiomas do leste asiático depende da configuração de localidade padrão do usuário no sistema operacional.

### <a name="writing-pad"></a>Painel de escrita

O painel de escrita é semelhante à interface do usuário familiar do painel de entrada.

O painel de escrita coleta manuscrito do usuário final. A interface do usuário básica inclui uma única linha de escrita na qual o usuário pode gravar texto com uma caneta digital. Quando o usuário terminar de gravar e tocar no botão enviar ou aguardar a ocorrência de um tempo limite, o manuscrito será enviado ao reconhecedor.

A tinta é reconhecida após uma quantidade especificada de tempo decorrido desde a hora em que o último traço de tinta foi coletado. Quando o tempo limite ocorre, a tinta é removida da superfície da coleção e o reconhecimento ocorre. O texto reconhecido é então inserido no controle ao qual o objeto [**PenInputPanel**](peninputpanel-class.md) está anexado.

### <a name="east-asian-multibox-pad"></a>Painel Multibox do leste asiático

A versão do leste asiático do painel de entrada da caneta exibe uma interface Multibox para inserir caracteres asiáticos. Ele fornece alternativas e é semelhante à interface do usuário do painel de entrada. Os usuários podem corrigir caracteres não reconhecidos tocando em uma caixa de escrita e selecionando o caractere correto em uma lista de alternativas na barra na parte superior do painel de entrada da caneta. Os botões de filtro estão disponíveis para restringir a lista de alternativas de reconhecimento a tipos de caracteres especificados, como símbolos.

As versões coreana e japonesa do painel de escrita têm uma chave de conversão além das teclas mini rápidas que são comuns a todas as capas de linguagem.

Para obter caracteres latinos no teclado de escrita para idiomas do leste asiático, defina a propriedade [**factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid) para aumentar a precisão do reconhecimento de caracteres latinos. Defina o membro de **dígito** do objeto [**factor**](factoid-constants.md) para caracteres numéricos ou o membro **OneChar** do objeto **factor** para caracteres alfabéticos e numéricos.

### <a name="quickkeys-keypads"></a>Teclados de QuickKeys

O painel de entrada de caneta fornece dois pequenos blocos de teclado para inserir símbolos e números.

### <a name="in-place-keyboard"></a>Teclado in-loco

O painel de entrada de caneta fornece um modo de teclado para situações em que o reconhecimento de manuscrito não é suficiente. Por exemplo, ao inserir uma senha ou um número de peça, os usuários provavelmente terão mais sucesso usando o teclado do painel de entrada da caneta do que fariam com o painel de escrita. Isso ocorre porque as senhas ou números de peça provavelmente estão no dicionário do reconhecedor do painel de escrita.

## <a name="recognizer-support"></a>Suporte do reconhecedor

o objeto [**PenInputPanel**](peninputpanel-class.md) dá suporte a reconhecedores de envio para Windows XP tablet pc Edition versão 1,0 e para o SDK do Tablet pc versão 1,5.

## <a name="automatic-positioning"></a>Posicionamento automático

Por padrão, o painel de entrada da caneta é posicionado automaticamente em relação ao controle ao qual ele está anexado. Ele não se sobrepõe ao controle, a menos que não haja espaço real de tela suficiente para o painel de entrada da caneta e o controle, ou a menos que o desenvolvedor defina explicitamente a posição do painel de entrada da caneta.

Funções de posicionamento automático somente quando o desenvolvedor não definiu a posição explicitamente usando o método [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) . Para substituir o posicionamento automático, altere os valores das propriedades [**superior**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**esquerda**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) em um manipulador de eventos [**PanelMoving**](peninputpanel-panelmoving.md) .

A posição do painel de entrada da caneta é restrita pelas bordas da tela. Nenhuma borda do painel de entrada da caneta pode ter mais de 0,25 polegadas a partir de qualquer borda da tela.

Por padrão, a parte superior do painel de entrada da caneta aparece na parte inferior do controle ao qual está anexada e é separada do controle pelo valor da propriedade [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset) . Se não houver espaço suficiente abaixo do controle, a parte inferior do painel de entrada da caneta aparecerá na parte superior do controle ao qual ele está anexado e será separada do controle pelo valor da propriedade **VerticalOffset** . Se ainda não houver espaço suficiente, como no caso de um controle de edição de tela inteira, o painel de entrada da caneta sobreporá o controle.

O painel de entrada da caneta esquerda aparece na borda esquerda do controle ao qual ele está anexado e é separado do controle pelo valor da propriedade [**as**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset) , exceto como limitado pela tela. Se a posição desejada colocar o painel de entrada da caneta além dos limites de tela disponíveis, o painel de entrada da caneta assumirá a posição horizontal mais próxima possível.

### <a name="forced-overlap"></a>Sobreposição forçada

Às vezes, é necessário que o painel de entrada da caneta se sobreponha ao controle anexado, como no caso de um controle de edição de tela inteira. Nesses casos, o posicionamento automático do painel de entrada da caneta é determinado usando as seguintes regras:

-   Quando o ponto de inserção está na metade superior do controle anexado, a posição vertical do painel de entrada da caneta fica na parte inferior da tela, possivelmente colocando-o na parte inferior do controle.
-   Quando o ponto de inserção está na metade inferior do controle anexado, a posição vertical do painel de entrada da caneta fica na parte superior da tela, possivelmente colocando-o na metade superior do controle.

### <a name="windowless-controls"></a>Controles sem janelas

No caso em que um objeto [**PenInputPanel**](peninputpanel-class.md) é anexado a um controle sem janela, o painel de entrada da caneta é posicionado em relação ao pai do controle sem janela. Defina as propriedades [**superior**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top) e [**esquerda**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left) em um manipulador de eventos [**PanelMoving**](peninputpanel-panelmoving.md) ou use o método [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) para posicionar manualmente o painel de entrada da caneta.

 

 
