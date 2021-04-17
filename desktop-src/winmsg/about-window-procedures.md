---
description: Cada janela é um membro de uma determinada classe de janela. A classe Window determina o procedimento de janela padrão que uma janela individual usa para processar suas mensagens.
ms.assetid: 3a8e8f4e-910d-4863-a4a7-dd37c2dfa402
title: Sobre os procedimentos de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f63586b9ca4ac6fe8486ba112316174533b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783780"
---
# <a name="about-window-procedures"></a>Sobre os procedimentos de janela

Cada janela é um membro de uma determinada classe de janela. A classe Window determina o procedimento de janela padrão que uma janela individual usa para processar suas mensagens. Todas as janelas que pertencem à mesma classe usam o mesmo procedimento de janela padrão. Por exemplo, o sistema define um procedimento de janela para a classe de caixa de combinação (**ComboBox**); em seguida, todas as caixas de combinação usam esse procedimento de janela.

Um aplicativo normalmente registra pelo menos uma nova classe de janela e seu procedimento de janela associado. Depois de registrar uma classe, o aplicativo pode criar muitas janelas dessa classe, todas as quais usam o mesmo procedimento de janela. Como isso significa que várias fontes poderiam chamar simultaneamente a mesma parte do código, você deve ter cuidado ao modificar recursos compartilhados de um procedimento de janela. Para obter mais informações, consulte [classes de janela](window-classes.md).

Os procedimentos de janela para caixas de diálogo (chamadas de procedimentos de caixa de diálogo) têm uma estrutura e função semelhantes como procedimentos de janela regular. Todos os pontos que se referem aos procedimentos de janela nesta seção também se aplicam aos procedimentos da caixa de diálogo. Para obter mais informações, consulte [caixas de diálogo](/windows/desktop/dlgbox/dialog-boxes).

Esta seção aborda os tópicos a seguir.

-   [Estrutura de um procedimento de janela](#structure-of-a-window-procedure)
-   [Procedimento de janela padrão](#default-window-procedure)
-   [Subclasse de procedimento de janela](#window-procedure-subclassing)
    -   [Subclasse de instância](#instance-subclassing)
    -   [Subclasse global](#global-subclassing)
-   [Superclasse de procedimento de janela](#window-procedure-superclassing)

## <a name="structure-of-a-window-procedure"></a>Estrutura de um procedimento de janela

Um procedimento de janela é uma função que tem quatro parâmetros e retorna um valor assinado. Os parâmetros consistem em um identificador de janela, um identificador de mensagem **uint** e dois parâmetros de mensagem declarados com os tipos de dados **wParam** e **lParam** . Para obter mais informações, consulte [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).

Os parâmetros de mensagem geralmente contêm informações em suas palavras de ordem inferior e de ordem superior. Há várias macros que um aplicativo pode usar para extrair informações dos parâmetros da mensagem. A macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) , por exemplo, extrai a palavra de ordem inferior (bits 0 a 15) de um parâmetro de mensagem. Outras macros incluem [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))e [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)).

A interpretação do valor de retorno depende da mensagem específica. Consulte a descrição de cada mensagem para determinar o valor de retorno apropriado.

Como é possível chamar um procedimento de janela recursivamente, é importante minimizar o número de variáveis locais que ele usa. Ao processar mensagens individuais, um aplicativo deve chamar funções fora do procedimento de janela para evitar o uso excessivo de variáveis locais, possivelmente causando o estouro da pilha durante a recursão profunda.

## <a name="default-window-procedure"></a>Procedimento de janela padrão

A função de procedimento de janela padrão, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , define determinado comportamento fundamental compartilhado por todas as janelas. O procedimento de janela padrão fornece a funcionalidade mínima para uma janela. Um procedimento de janela definido pelo aplicativo deve passar todas as mensagens que ele não processa para a função **DefWindowProc** para processamento padrão.

## <a name="window-procedure-subclassing"></a>Subclasse de procedimento de janela

Quando um aplicativo cria uma janela, o sistema aloca um bloco de memória para armazenar informações específicas para a janela, incluindo o endereço do procedimento de janela que processa as mensagens da janela. Quando o sistema precisa passar uma mensagem para a janela, ele pesquisa as informações específicas da janela para o endereço do procedimento de janela e passa a mensagem para esse procedimento.

A *subclasse* é uma técnica que permite que um aplicativo intercepte e processe mensagens enviadas ou postadas em uma janela específica antes que a janela tenha a oportunidade de processá-las. Por meio da subclasse de uma janela, um aplicativo pode aumentar, modificar ou monitorar o comportamento da janela. Um aplicativo pode subclasser uma janela que pertence a uma classe global do sistema, como um controle de edição ou uma caixa de listagem. Por exemplo, um aplicativo poderia subclasser um controle de edição para impedir que o controle aceite determinados caracteres. No entanto, você não pode fazer uma subclasse de uma janela ou classe que pertença a outro aplicativo. Todas as subclasses devem ser executadas no mesmo processo.

Um aplicativo faz uma subclasse de uma janela substituindo o endereço do procedimento de janela original da janela pelo endereço de um novo procedimento de janela, chamado de *procedimento de subclasse*. Depois disso, o procedimento de subclasse recebe todas as mensagens enviadas ou postadas na janela.

O procedimento de subclasse pode executar três ações após o recebimento de uma mensagem: ela pode passar a mensagem para o procedimento de janela original, modificar a mensagem e passá-la para o procedimento de janela original ou processar a mensagem e não passá-la para o procedimento de janela original. Se o procedimento de subclasse processar uma mensagem, ele poderá fazer isso antes, depois ou antes e depois de passar a mensagem para o procedimento de janela original.

O sistema fornece dois tipos de subclasses: [instância](#instance-subclassing) e [global](#global-subclassing). Na *subclasse de instância*, um aplicativo substitui o endereço de procedimento de janela de uma única instância de uma janela. Um aplicativo deve usar subclasse de instância para subclasse de uma janela existente. Em uma *subclasse global*, um aplicativo substitui o endereço do procedimento de janela na estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) de uma classe de janela. Todas as janelas subsequentes criadas com a classe têm o endereço do procedimento de subclasse, mas as janelas existentes da classe não são afetadas.

### <a name="instance-subclassing"></a>Subclasse de instância

Um aplicativo subclasse uma instância de uma janela usando a função [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) . O aplicativo passa o **sinalizador \_ WndProc GWL** , o identificador para a janela para subclasse e o endereço do procedimento de subclasse para **SetWindowLong**. O procedimento de subclasse pode residir tanto no executável do aplicativo quanto em uma DLL.

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) retorna o endereço do procedimento de janela original da janela. O aplicativo deve salvar o endereço, usando-o em chamadas subsequentes para a função [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) , para passar mensagens interceptadas para o procedimento de janela original. O aplicativo também deve ter o endereço do procedimento de janela original para remover a subclasse da janela. Para remover a subclasse, o aplicativo chama **SetWindowLong** novamente, passando o endereço do procedimento de janela original com o sinalizador **GWL \_ WndProc** e o identificador para a janela.

O sistema possui as classes globais do sistema, e aspectos dos controles podem mudar de uma versão do sistema para a próxima. Se o aplicativo deve subclasser uma janela que pertence a uma classe global do sistema, talvez o desenvolvedor precise atualizar o aplicativo quando uma nova versão do sistema for liberada.

Como a subclasse de instância ocorre depois que uma janela é criada, você não pode adicionar nenhum byte extra à janela. Aplicativos que a subclasse a Window deve usar a lista de propriedades da janela para armazenar os dados necessários para uma instância da janela de subclasse. Para obter mais informações, consulte [Propriedades da janela](window-properties.md).

Quando um aplicativo subclasse uma janela de subclasse, ele deve remover as subclasses na ordem inversa em que foram executadas. Se a ordem de remoção não for revertida, poderá ocorrer um erro irrecuperável do sistema.

### <a name="global-subclassing"></a>Subclasse global

Para fazer uma subclasse global de uma classe de janela, o aplicativo deve ter um identificador para uma janela da classe. O aplicativo também precisa do identificador para remover a subclasse. Para obter o identificador, um aplicativo normalmente cria uma janela oculta da classe a ser subclasse. Depois de obter o identificador, o aplicativo chama a função [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) , especificando o identificador, o sinalizador **\_ WndProc GCL** e o endereço do procedimento de subclasse. **SetClassLong** retorna o endereço do procedimento de janela original para a classe.

O endereço do procedimento de janela original é usado em subclasse global da mesma forma que é usado na subclasse da instância. O procedimento de subclasse passa mensagens para o procedimento de janela original chamando [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca). O aplicativo remove a subclasse da classe Window chamando [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) novamente, especificando o endereço do procedimento de janela original, o sinalizador **\_ WndProc GCL** e o identificador para uma janela da classe que está sendo subclasse. Um aplicativo que globalmente subclasse uma classe de controle deve remover a subclasse quando o aplicativo é encerrado; caso contrário, pode ocorrer um erro irrecuperável do sistema.

A subclasse global tem as mesmas limitações que a subclasse de instância, além de algumas restrições adicionais. Um aplicativo não deve usar os bytes extras para a classe ou a instância de janela sem saber exatamente como o procedimento de janela original os utiliza. Se o aplicativo precisar associar dados a uma janela, ele deverá usar as propriedades da janela.

## <a name="window-procedure-superclassing"></a>Superclasse de procedimento de janela

A *superclasseing* é uma técnica que permite que um aplicativo crie uma nova classe de janela com a funcionalidade básica da classe existente, além de aprimoramentos fornecidos pelo aplicativo. Uma superclasse é baseada em uma classe de janela existente chamada *classe base*. Frequentemente, a classe base é uma classe de janela global do sistema, como um controle de edição, mas pode ser qualquer classe de janela.

Uma superclasse tem seu próprio procedimento de janela, chamado de procedimento de superclasse. O *procedimento de superclasse* pode executar três ações após o recebimento de uma mensagem: ela pode passar a mensagem para o procedimento de janela original, modificar a mensagem e passá-la para o procedimento de janela original ou processar a mensagem e não passá-la para o procedimento de janela original. Se o procedimento de superclasse processa uma mensagem, ele pode fazer isso antes, depois ou antes e depois de passar a mensagem para o procedimento de janela original.

Ao contrário de um procedimento de subclasse, um procedimento de superclasse pode processar mensagens de criação de janela ([**WM \_ NCCREATE**](wm-nccreate.md), [**WM \_ Create**](wm-create.md)e assim por diante), mas também deve passá-las para o procedimento de janela de classe base original para que o procedimento de janela de classe base possa executar seu procedimento de inicialização.

Para superclassear uma classe de janela, um aplicativo primeiro chama a função [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) para recuperar informações sobre a classe base. **GetClassInfo** preenche uma estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) com os valores da estrutura **WNDCLASS** da classe base. Em seguida, o aplicativo copia seu próprio identificador de instância para o membro **HINSTANCE** da estrutura **WNDCLASS** e copia o nome da superclasse no membro **lpszClassName** . Se a classe base tiver um menu, o aplicativo deverá fornecer um novo menu com os mesmos identificadores de menu e copiar o nome do menu para o membro **lpszMenuName** . Se o procedimento de superclasse processar a mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) e não passá-la para o procedimento de janela da classe base, o menu não precisará ter identificadores correspondentes. **GetClassInfo** não retorna o membro **lpszMenuName**, **LpszClassName** ou **HINSTANCE** da estrutura **WNDCLASS** .

Um aplicativo também deve definir o membro **lpfnWndProc** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . A função [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) preenche esse membro com o endereço do procedimento de janela original para a classe. O aplicativo deve salvar esse endereço, para passar mensagens para o procedimento de janela original e, em seguida, copiar o endereço do procedimento de superclasse no membro **lpfnWndProc** . O aplicativo pode, se necessário, modificar quaisquer outros membros da estrutura **WNDCLASS** . Depois de preencher a estrutura **WNDCLASS** , o aplicativo registra a superclasse passando o endereço da estrutura para a função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . A superclasse pode ser usada para criar o Windows.

Como a superclasse registra uma nova classe de janela, um aplicativo pode adicionar tanto os bytes de classe extras quanto os bytes de janela extras. A superclasse não deve usar os bytes extras originais para a classe base ou a janela pelos mesmos motivos para que uma subclasse de instância ou uma subclasse global não deva usá-las. Além disso, se o aplicativo Adicionar bytes extras para seu uso na classe ou na instância de janela, ele deverá referenciar os bytes extras relativos ao número de bytes extras usados pela classe base original. Como o número de bytes usados pela classe base pode variar de uma versão da classe base para a próxima, o deslocamento inicial para os próprios bytes extras da superclasse também pode variar de uma versão da classe base para a próxima.

 

 
