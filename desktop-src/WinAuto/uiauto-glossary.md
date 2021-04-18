---
title: Glossário (recursos de acessibilidade do Windows)
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c45583f2-a6e8-4a01-9577-9b604b5bbc62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16679c63f0716058e53c7c9d164a24593c481dff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105779933"
---
# <a name="glossary-windows-accessibility-features"></a>Glossário (recursos de acessibilidade do Windows)

## <a name="a"></a>Um

<dl> <dt>

**chave de acesso**
</dt> <dd>

Um caractere sublinhado no texto do rótulo de um controle.

</dd> <dt>

**auxílio de acessibilidade**
</dt> <dd>

Também chamada de tecnologia assistencial; programas especializados que funcionam com o sistema operacional de um computador para acomodar deficiências específicas, como um intervalo limitado de movimento ou cegueira. Os produtos incluem teclados maiores, teclados olhar operativos, utilitários de entrada de voz, teclados na tela e produtos que podem converter texto em fala ou em uma exibição em Braille dinâmica. Para obter mais informações, consulte [produtos de tecnologia assistencial](https://www.microsoft.com/enable/at/default.aspx).

</dd> <dt>

**objeto acessível**
</dt> <dd>

Qualquer elemento de interface do usuário que implementa a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e tem propriedades que descrevem o nome do objeto, locais da tela e outras informações necessárias para auxílios de acessibilidade. Para obter mais informações, consulte [objetos acessíveis](accessible-objects.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**elemento filho**
</dt> <dd>

Consulte [*elemento simples*](uiauto-glossary.md).

</dd> <dt>

**cliente**
</dt> <dd>

Qualquer programa que usa a automação da interface do usuário ou o Microsoft Acessibilidade Ativa para acessar, identificar ou manipular os elementos da interface de usuários de um aplicativo; Os clientes incluem auxílios de acessibilidade, ferramentas de teste automatizadas e alguns aplicativos de treinamento baseados em computador. Para obter mais informações, consulte [como acessibilidade ativa funciona](how-active-accessibility-works.md).

</dd> <dt>

**provedor do lado do cliente**
</dt> <dd>

Um componente de software que é implementado por um cliente de automação de interface do usuário para recuperar informações sobre a interface do usuário de um aplicativo que não dá suporte a, ou não dá suporte total à automação da interface do usuário. Normalmente, os provedores do lado do cliente (proxies) se comunicam com o aplicativo pelo limite do processo enviando e recebendo mensagens do Windows.

</dd> <dt>

**contêiner**
</dt> <dd>

Também chamado de pai; um objeto acessível que corresponde a um ou mais elementos simples; por exemplo, um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para uma caixa de listagem é o pai dos itens de lista.

</dd> <dt>

**padrão de controle**
</dt> <dd>

Na automação da interface do usuário, uma implementação de design que descreve uma parte de funcionalidade discreta para um controle. Essa funcionalidade pode incluir a aparência visual de um controle e as ações que ele pode executar.

</dd> <dt>

**objeto de padrão de controle**
</dt> <dd>

Uma instância de tempo de execução de um objeto COM que expõe uma ou mais interfaces de padrão de controle.

</dd> <dt>

**provedor de padrão de controle**
</dt> <dd>

Um componente de software que implementa uma ou mais interfaces de padrão de controle.

</dd> <dt>

**controle personalizado**
</dt> <dd>

Um controle criado por um usuário ou fornecedor de software de terceiros, ou um controle definido pelo sistema que foi modificado por um usuário ou fornecedor de software de terceiros.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**degenerar intervalo de texto (intervalo vazio)**
</dt> <dd>

Um objeto que representa um intervalo de texto vazio (sem caracteres). Um intervalo de texto de degenerado tem pontos de extremidade adjacentes e especifica um ponto entre dois caracteres.

</dd> <dt>

**intervalo de texto não contíguo**
</dt> <dd>

Um objeto que representa várias extensões de texto que não estão fisicamente adjacentes entre si.

</dd> <dt>

**contêiner de encaixe**
</dt> <dd>

Um controle que permite a organização de elementos filho, tanto horizontal quanto verticalmente, em relação aos limites do contêiner de encaixe e a outros elementos dentro do contêiner.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**ouvinte de eventos**
</dt> <dd>

Um aplicativo cliente que foi registrado para receber notificações da automação da interface do usuário ou do Microsoft Acessibilidade Ativa sempre que ocorrem alterações específicas da interface do usuário.

</dd> <dt>

**notificação de eventos**
</dt> <dd>

Uma chamada de um provedor de automação de interface do usuário para um cliente, na qual o provedor notifica o cliente sobre um evento que pode afetar o estado ou a aparência de um item da interface do usuário.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filtrar \[ ing\]**
</dt> <dd>

Para definir os tipos de elementos de automação da interface do usuário a serem incluídos em uma exibição da árvore de automação da interface do usuário. Consulte também: exibição bruta, exibição de controle e exibição de conteúdo.

</dd> <dt>

**raiz do fragmento**
</dt> <dd>

O elemento de automação da interface do usuário no nó raiz de uma subárvore da árvore de automação da interface do usuário. Uma raiz de fragmento não tem um pai, mas está hospedada em alguma outra estrutura, geralmente um identificador de janela do Win32 (**HWND**).

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**hospedeira**
</dt> <dd>

Um elemento de interface do usuário, como uma janela ou controle, que contém outros elementos da interface do usuário. Um host executa serviços de automação de interface do usuário em nome dos elementos hospedados.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**IAccessible**
</dt> <dd>

A interface COM que contém todos os métodos e propriedades do Microsoft Acessibilidade Ativa.

</dd> <dt>

**Proxy de IAccessible**
</dt> <dd>

Um tipo de suporte do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que fornece informações de acessibilidade padrão para elementos de interface do usuário padrão: controles de usuários, menus de usuário e controles comuns de COMCTL e Comctl32. Para obter mais informações, consulte [proxies do IAccessible](iaccessible-proxies.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**navegação lógica**
</dt> <dd>

Um dos dois modos de navegação [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nos quais um cliente explora a hierarquia de objetos do Microsoft acessibilidade ativa (próximo, anterior, pai, primeiro filho, último filho).

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**marshaling**
</dt> <dd>

Empacotando e enviando parâmetros de interface entre limites de processo.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**implementação nativa**
</dt> <dd>

O tipo de suporte fornecido pelos elementos da interface do usuário que implementam a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**modelo fora da tela**
</dt> <dd>

Esse modelo é um banco de dados de objetos na tela e inclui suas propriedades e suas relações espaciais.

</dd> <dt>

**OLEACC**
</dt> <dd>

A biblioteca de vínculo dinâmico que fornece o tempo de execução da Microsoft Acessibilidade Ativa e gerencia solicitações de clientes do Microsoft Acessibilidade Ativa.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**parent**
</dt> <dd>

Também chamado de contêiner; um objeto acessível que corresponde a um ou mais elementos simples; por exemplo, um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para uma caixa de listagem é o pai dos itens de lista

</dd> <dt>

**elemento PlaceHolder de automação**
</dt> <dd>

Um elemento de automação da interface do usuário que representa um item virtualizado na árvore de automação da interface do usuário. Normalmente, um espaço reservado não tem dados carregados para todas as propriedades de automação da interface do usuário e é necessário implementar apenas o padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .

</dd> <dt>

**evento de alteração de propriedade**
</dt> <dd>

Um evento que é disparado quando o valor de uma propriedade é alterado. Os clientes se registram para receber eventos de alteração de propriedade específicos e a automação da interface do usuário notifica os clientes registrados quando esses eventos ocorrem.

</dd> <dt>

**interface do provedor**
</dt> <dd>

Uma coleção de métodos públicos implementados por um provedor de automação de interface do usuário.

</dd> <dt>

**acionista**
</dt> <dd>

Consulte [*proxy IAccessible*](uiauto-glossary.md).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**exibição bruta**
</dt> <dd>

A árvore completa de objetos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) na árvore de automação da interface do usuário para a qual a área de trabalho é a raiz. A exibição bruta segue melhor a estrutura programática nativa de um aplicativo e, portanto, é a exibição mais precisa da estrutura da interface do usuário. Também é a base na qual as outras exibições da árvore são criadas.

</dd> <dt>

**item realizado**
</dt> <dd>

Um item de interface do usuário para o qual informações completas foram carregadas na memória, permitindo que a automação da interface do usuário crie um elemento de automação para o item.

</dd> <dt>

**identificador de tempo de execução**
</dt> <dd>

Uma matriz de inteiros que identifica a instância em execução de um elemento de automação da interface do usuário. O identificador é exclusivo na interface do usuário da área de trabalho na qual foi gerado.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**matriz segura**
</dt> <dd>

Um tipo de dados autodescritivo para declarar matrizes usadas na criação de componentes COM. Junto com os dados, uma matriz segura contém informações sobre o número e limites de suas dimensões.

</dd> <dt>

**cedido**
</dt> <dd>

Definindo a extensão da exibição, a partir de um elemento base.

</dd> <dt>

**server**
</dt> <dd>

Qualquer controle, módulo ou aplicativo que usa o Microsoft Acessibilidade Ativa para expor informações sobre sua interface do usuário

</dd> <dt>

**provedor do lado do servidor**
</dt> <dd>

Um componente de software que expõe informações sobre um elemento de interface do usuário baseado em uma estrutura de interface do usuário que não oferece suporte nativo à automação da interface do usuário. Provedores do lado do servidor (provedores nativos) se comunicam com aplicativos cliente durante o limite do processo expondo interfaces COM ao sistema de núcleo de automação da interface do usuário, que serviços solicita de clientes.

</dd> <dt>

**elemento simples**
</dt> <dd>

Também conhecido como elemento filho; qualquer elemento de interface do usuário que compartilha um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com outros elementos e depende desse objeto **IAccessible** para expor suas propriedades. Para obter mais informações, consulte [elementos simples](simple-elements.md).

</dd> <dt>

**navegação espacial**
</dt> <dd>

Um dos dois modos de navegação [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nos quais um cliente passa de um elemento de interface do usuário para outro com base em suas posições na tela (para cima, para baixo, para a esquerda e para a direita).

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Estrutura de serviços de texto**
</dt> <dd>

Uma estrutura de sistema escalonável que permite serviços de linguagem natural e entrada de texto avançada na área de trabalho e em aplicativos.

</dd> <dt>

**unidade de texto**
</dt> <dd>

Uma unidade de texto predefinida (caractere, palavra, linha ou parágrafo) usada para navegar por segmentos lógicos de um intervalo de texto.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Cliente de automação da interface do usuário**
</dt> <dd>

Um aplicativo de tecnologia assistencial, como um leitor de tela, que usa a automação da interface do usuário para obter acesso programático aos elementos da interface do usuário em uma interface de usuários do aplicativo. O cliente apresenta informações sobre os elementos da interface do usuário para os usuários finais. Scripts de teste automatizados também são considerados clientes de automação da interface do usuário.

</dd> <dt>

**Núcleo de automação da interface do usuário**
</dt> <dd>

Um componente de tempo de execução que implementa a estrutura de automação da interface do usuário.

</dd> <dt>

**Elemento de automação da interface do usuário**
</dt> <dd>

Um item de interface do usuário que é representado por um objeto COM que implementa uma interface do provedor de automação de interface do usuário e que expõe a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para clientes de automação da interface do usuário.

</dd> <dt>

**Estrutura de automação da interface do usuário**
</dt> <dd>

Um componente integral do Windows que dá suporte ao acesso programático à maioria dos elementos da interface do usuário na área de trabalho. Ele permite que produtos de tecnologia assistencial, como leitores de tela, forneçam informações sobre a interface do usuário aos usuários finais e manipulem a interface do usuário por meio de uma entrada padrão. A automação da interface do usuário também permite que scripts de teste automatizados interajam com a interface do usuário

</dd> <dt>

**Nó de automação da interface do usuário**
</dt> <dd>

Preterido. Consulte elemento de automação da interface do usuário.

</dd> <dt>

**Provedor de automação de interface do usuário**
</dt> <dd>

Uma implementação de interfaces de automação da interface do usuário que expõe informações programáticas sobre um elemento de interface do usuário. O provedor fornece essas informações para a estrutura de automação da interface do usuário em resposta às solicitações de cliente de automação da interface do usuário.

</dd> <dt>

**Árvore de automação da interface do usuário**
</dt> <dd>

Uma representação hierárquica de todos os elementos de automação da interface do usuário na área de trabalho do Windows. A árvore consiste em um elemento raiz que representa a área de trabalho atual e cujos elementos filho representam janelas de aplicativo. Cada um desses elementos filho pode conter elementos que representam partes da interface do usuário, como menus, botões, barras de ferramentas e caixas de listagem. Esses elementos podem conter elementos como itens de lista.

</dd> <dt>

**Estrutura de interface do usuário**
</dt> <dd>

Um componente que gerencia controles filho, testes de clique e renderização em uma área da tela.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**identificador de exibição**
</dt> <dd>

Um valor que identifica uma exibição que está disponível para um elemento de automação da interface do usuário que implementa um padrão de controle. Esse tipo de elemento fornece e é capaz de alternar entre as várias representações do mesmo conjunto de informações ou controles filho.

</dd> <dt>

**item virtualizado**
</dt> <dd>

Um elemento de interface do usuário que é carregado na memória somente quando é necessário, normalmente quando o elemento fica visível na tela. Um item virtualizado é representado por um elemento de automação de espaço reservado na árvore de automação da interface do usuário.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Eventos de janela (WinEvents)**
</dt> <dd>

O tipo de evento usado para notificar os clientes de que um objeto acessível foi alterado de alguma maneira.

</dd> <dt>

**elemento baseado em janela**
</dt> <dd>

Um elemento de automação de interface do usuário que representa um item de interface do usuário que tem seu próprio identificador de janela do Win32 (**HWND**).

</dd> </dl>

 

 




