---
title: Ferramentas de acessibilidade-AccEvent (Inspetor de eventos acessível)
description: AccEvent (Inspetor de eventos acessível) permite que os desenvolvedores e testadores validem que os elementos da interface do usuário do aplicativo disparam a automação da interface do usuário da Microsoft e eventos do Microsoft Acessibilidade Ativa quando ocorrem alterações na interface do usuário.
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2192bf6973444bf2bfc307ff4613d9d1c593d5a22f9800ecb61bc310b3a210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327794"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>Ferramentas de acessibilidade-AccEvent (Inspetor de eventos acessível)

**AccEvent (Inspetor de eventos acessível)** permite que os desenvolvedores e testadores validem que os elementos da interface do usuário do aplicativo disparam a automação da interface do usuário da Microsoft e eventos do Microsoft acessibilidade ativa quando ocorrem alterações na interface do usuário. As alterações na interface do usuário podem ocorrer quando o foco é alterado ou quando um elemento de interface do usuário é invocado, selecionado ou tem uma alteração de estado ou propriedade.

o **AccEvent** é instalado com o SDK (Software Development Kit) do Windows. Ele está localizado na \\ pasta bin \\ < *version* > \\ < > do caminho de instalação do SDK (Accevent.exe).

> [!NOTE]
> **AccEvent** é uma ferramenta herdada. é recomendável usar [Insights de acessibilidade](https://accessibilityinsights.io/) em vez disso.

## <a name="requirements"></a>Requisitos

O **AccEvent** pode ser usado para examinar dados de acessibilidade em sistemas que não têm a automação da interface do usuário, foi escrito originalmente para o Microsoft acessibilidade ativa. Para examinar a automação da interface do usuário, a automação da interface do usuário deve estar presente no sistema. Para obter mais informações, consulte a seção "requisitos" da [automação da interface do usuário](entry-uiauto-win32.md).

o **AccEvent** é instalado como parte do conjunto geral de ferramentas no SDK do Windows, ele não é distribuído como um download de exe separado. o SDK do Windows inclui todas as ferramentas relacionadas à acessibilidade documentadas nesta seção. [obtenha o SDK do Windows.](https://developer.microsoft.com/) (Há também um arquivo de download do SDK vinculado dessa página, se você precisar de uma versão anterior.)

Para executar o **AccEvent**, localize AccEvent.exe na \\ pasta bin \\ < *version* > \\ < > e execute-o (normalmente, você não precisa executar como administrador).

## <a name="the-accessible-event-watcher-window"></a>A janela do Inspetor de eventos acessível

Quando você inicia o **AccEvent**, a janela principal é exibida. A janela principal do **AccEvent** exibe a automação da interface do usuário ou os eventos do Microsoft acessibilidade ativa gerados por aplicativos que estão executando o. A janela principal tem as seguintes partes principais:

- Barra de título. Exibe o estado e o modo de operação atual.
- Barra de menus. Fornece acesso à funcionalidade do **AccEvent** .
- Exibição de dados. Exibe informações sobre cada evento, incluindo a ID do evento e as propriedades selecionadas do elemento de interface do usuário que gerou o evento.

**AccEvent** tem apenas uma interface gráfica do usuário; Não há nenhum argumento de linha de comando para essa ferramenta, mas você pode usar outras ferramentas para processar o log de saída como texto.

A imagem a seguir mostra a janela principal do **AccEvent** .

![a interface do usuário para a ferramenta de Inspetor de eventos acessível](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>Tarefas de Inspetor de eventos acessíveis

Esta seção inclui informações sobre as tarefas **AccEvent** usadas com frequência.

### <a name="configuring-the-operating-mode"></a>Configurando o modo de operação

Use o menu **modo** para configurar o modo de operação **AccEvent** e selecione as configurações que controlam o comportamento da ferramenta. Você pode selecionar as opções a seguir.



| Quando essa opção é selecionada | **AccEvent** faz isso                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sempre no início                | Aparece na parte superior de qualquer outra interface do usuário na tela.                                                                                                                                                                                    |
| Eventos UIA                   | Exibe informações sobre eventos de automação da interface do usuário.                                                                                                                                                                                             |
| WinEvents (no contexto)       | Exibe informações sobre eventos do Microsoft Acessibilidade Ativa (WinEvents) passados para funções de Hook que residem no espaço de endereço do servidor. Para obter mais informações, consulte [funções de gancho no contexto](in-context-hook-functions.md).         |
| WinEvents (fora do contexto)   | Exibe informações sobre eventos do Microsoft Acessibilidade Ativa (WinEvents) passados para funções de Hook que residem no espaço de endereço do cliente. Para obter mais informações, consulte [funções de gancho fora do contexto](out-of-context-hook-functions.md). |
| Mostrar retângulo de realce     | Realça um retângulo em volta do elemento de interface do usuário que gerou o evento selecionado.                                                                                                                                                                 |
| Mostrar dica de ferramenta de informações     | Mostra informações de evento em uma dica de ferramenta.                                                                                                                                                                                                        |
| Configurações                     | exibe a caixa de diálogo **Configurações de evento UIA** ou **Configurações de WinEvent** .                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>Filtrando eventos de automação da interface do usuário

para configurar os eventos de automação da interface do usuário e as propriedades que são exibidas na janela **AccEvent** , clique no menu **modo** , selecione **eventos UIA** e, em seguida, selecione **Configurações**. a caixa de diálogo **Configurações de evento UIA** é exibida. Você também pode usar essa caixa de diálogo para filtrar eventos.

a caixa de diálogo **Configurações de evento UIA** contém os seguintes painéis:

- **Eventos globais**

    Marque a caixa de seleção **FocusChangedEvent** para exibir informações sobre eventos de alteração de foco global.

- **Tipo de evento**

    Selecione os eventos nos quais você está interessado.

- **Escopo**

    Selecione o elemento de interface do usuário que você deseja que o **AccEvent** Ouça para eventos.

- **Incluir eventos de**

    Selecione **filhos imediatos** se você quiser ver os eventos dos elementos filho imediatos do elemento de interface do usuário selecionado no painel **escopo** . Se você quiser ver eventos de todos os elementos descendentes, selecione **todos os descendentes**.

- **Propriedades de relatório**

    Selecione as propriedades que você deseja exibir após cada evento na janela principal. Se a **dica de ferramenta mostrar informações** estiver selecionada no menu **modo** , as propriedades selecionadas também serão exibidas em uma dica de ferramenta.

### <a name="filtering-active-accessibility-events"></a>Filtrando eventos de Acessibilidade Ativa

para configurar os eventos e as propriedades do Microsoft Acessibilidade Ativa que são exibidos na janela **AccEvent** , clique no menu **modo** , selecione **WinEvents (no contexto)** ou **WinEvents (fora do contexto)** e, em seguida, selecione **Configurações**. a caixa de diálogo **Configurações de WinEvent** é exibida. Você também pode usar essa caixa de diálogo para filtrar eventos.

a caixa de diálogo **Configurações de WinEvent** contém os seguintes painéis:

- **Objetos**

    Selecione os objetos que você deseja que o **AccEvent** Ouça para eventos. O **AccEvent** pode escutar eventos provenientes do Windows, do cursor ou do cursor. A **janela** é selecionada por padrão.

- **Eventos**

    Selecione os eventos nos quais você está interessado. Todos os eventos são exibidos por padrão.

- **Informações do evento**

    Selecione as informações que você deseja exibir após cada nome de evento na janela principal.

- **Propriedades de objeto**

    Selecione as propriedades que você deseja exibir após cada evento na janela principal. Se a **dica de ferramenta mostrar informações** estiver selecionada no menu **modo** , as propriedades selecionadas também serão exibidas em uma dica de ferramenta. **Nome**, **função** e **estado** são selecionados por padrão.

- **Filtragem**

    Selecione um dos botões de opção na seção filtragem para filtrar os eventos gerados pelas janelas especificadas no campo **HWNDs** . O botão de opção **não filtrar** é selecionado por padrão.

    - Selecione o botão de opção **excluir** para exibir somente os eventos gerados de objetos diferentes das janelas especificadas.
    - Selecione o botão de opção **incluir apenas** e especifique um ou mais identificadores de janela para exibir apenas os eventos gerados por essas janelas.
    - Marque a caixa de seleção **e descendentes** para incluir eventos gerados pelos descendentes das janelas especificadas.

- **Opções**

    Selecione qualquer uma das seguintes opções:

    

    | Quando essa opção é selecionada                                  | **AccEvent** faz isso                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Usar invocação                                                    | Usa [IDispatch::Invoke para](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) recuperar propriedades de objeto em vez de usar [**métodos IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                               |
    | Sempre Obter Objeto (mesmo que nenhuma propriedade de objeto seja selecionada)     | Recupera o objeto associado ao evento mesmo que nenhum item seja selecionado no painel Propriedades do Objeto.                                                                                        |
    | Exibir a propriedade padrão (além das propriedades selecionadas) | Exibe a propriedade padrão, se alguma, para o objeto associado ao evento, juntamente com os itens selecionados no painel Propriedades do Objeto.                                                      |
    | Exibir informações de evento de janelas invisíveis/ocultas       | Exibe os itens selecionados no painel Informações do Evento para todos os objetos, incluindo aqueles em janelas invisíveis ou ocultas.                                                                       |
    | Exibir informações completas de eventos de janelas invisíveis/ocultas  | Exibe os itens selecionados no painel Informações do Evento e os itens selecionados (ou padrão) do painel Propriedades do Objeto, para todos os objetos, incluindo aqueles em janelas invisíveis ou ocultas. |
    | DebugBreak no próximo evento                                      | Faz com que uma exceção de ponto de interrupção ocorra no processo que origina o próximo WinEvent. Isso sinaliza o depurador para lidar com a exceção.                                                        |

### <a name="using-the-event-menu"></a>Usando o Menu de Eventos

Use **o** menu Evento para executar as seguintes tarefas:

| Quando essa opção é selecionada | **AccEvent** faz isso                                    |
|------------------------------|-------------------------------------------------------|
| Iniciar a escuta              | Inicia a exibição de informações de evento na exibição Dados. |
| Parar de escutar               | Interrompe a exibição de informações de evento na exibição Dados.  |
| Limpar histórico de eventos          | Limpa o conteúdo da exibição Dados.                 |
| Selecionar Todos os Eventos            | Seleciona todos os eventos listados na exibição Dados.           |
| Copiar eventos selecionados         | Copia os eventos selecionados para a área de transferência.          |

### <a name="saving-active-accessibility-events"></a>Salvando Acessibilidade Ativa eventos

Para começar a salvar eventos em um arquivo de texto, abra o menu **Arquivo** e **selecione Iniciar Registro em Log no Arquivo**. **AccEvent** começa a escrever eventos no arquivo especificado até que você selecione **Parar** Registro **em** Log no menu Arquivo. O arquivo de texto pode ser útil para solucionar problemas e revisar os eventos posteriormente.

## <a name="related-topics"></a>Tópicos relacionados

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Ferramentas de teste](testing-tools.md)
- [UI Accessibility Checker](ui-accessibility-checker.md)
- [Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
- [Verificação da Automação da Interface do Usuário](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)