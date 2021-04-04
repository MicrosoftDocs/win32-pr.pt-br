---
title: Imprimir folha de propriedades
description: A folha de propriedades Imprimir é uma interface de usuário padrão que permite ao usuário especificar as propriedades de um trabalho de impressão específico.
ms.assetid: b52b71cc-a583-4a21-8a53-501ab442e6f8
keywords:
- Interface do usuário do Windows, entrada do usuário
- Interface do usuário do Windows, biblioteca de caixa de diálogo comum
- entrada do usuário, biblioteca de caixa de diálogo comum
- capturando entrada do usuário, biblioteca de caixa de diálogo comum
- Biblioteca de caixa de diálogo comum
- caixas de diálogo comuns
- Caixa de diálogo Imprimir folha de propriedades
- Personalizando a caixa de diálogo Imprimir folha de propriedades
- caixas de diálogo predefinidas
- caixas de diálogo, imprimir folha de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20905f76af290b3978bec828a382604147297998
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008334"
---
# <a name="print-property-sheet"></a>Imprimir folha de propriedades

A folha de propriedades **Imprimir** é uma interface de usuário padrão que permite ao usuário especificar as propriedades de um trabalho de impressão específico. A folha de propriedades é composta por um conjunto de páginas de propriedades que varia de acordo com a impressora ou o aplicativo. Para um subconjunto de páginas de propriedades padrão do Windows, algumas impressoras podem adicionar páginas de propriedades específicas do driver e alguns aplicativos podem adicionar páginas de propriedades específicas do aplicativo.

Para criar e exibir uma folha de propriedades de **impressão** , inicialize uma estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) e passe a estrutura para a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) .

A ilustração a seguir mostra uma folha de propriedades de **impressão** típica.

![folha de propriedades da impressora](images/printerpropertypagexp.png)

A maioria dos membros da estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) é idêntica àquelas da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Para obter descrições de como usar os membros da estrutura comum para interagir com os controles da caixa de diálogo, consulte a [caixa de diálogo Imprimir](print-dialog-box.md). O restante deste tópico descreve os recursos de folha de propriedades de **impressão** que diferem da caixa de diálogo **Imprimir** .

Você pode personalizar uma folha de propriedades de **impressão** especificando um modelo de caixa de diálogo personalizada para a parte inferior da página **geral** e especificando páginas de propriedades adicionais para seguir a página **geral** . Para obter mais informações, consulte [Personalizando a folha de propriedades Imprimir](#customizing-the-print-property-sheet).

Você pode implementar um objeto de retorno de chamada para receber notificações e mensagens da função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) enquanto a folha de propriedades é exibida. Os aplicativos que fornecem modelos personalizados ou páginas adicionais usam o objeto de retorno de chamada para se comunicar com a folha de propriedades. Para obter mais informações, consulte [retorno de chamada do objeto para a folha de propriedades Imprimir](#callback-object-for-the-print-property-sheet).

A folha de propriedades **Imprimir** fornece suporte para especificar vários intervalos de páginas não contíguas a serem impressos. O membro **lpPageRanges** da estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) especifica uma matriz de estruturas [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) nas quais cada estrutura especifica um intervalo de páginas.

A folha de propriedades **Imprimir** exibe um botão de opção **página atual** como parte do grupo de **intervalos de página** de botões de opção. Para controlar o botão de opção **página atual** , use os sinalizadores **PD \_ CURRENTPAGE** e **PD \_ NOCURRENTPAGE** no membro **flags** da estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) .

Esta seção aborda os tópicos a seguir.

-   [Personalizando a folha de propriedades de impressão](#customizing-the-print-property-sheet)
-   [Objeto de retorno de chamada para a folha de propriedades de impressão](#callback-object-for-the-print-property-sheet)

## <a name="customizing-the-print-property-sheet"></a>Personalizando a folha de propriedades de impressão

Você pode personalizar a folha de propriedades de **impressão** das seguintes maneiras:

-   Forneça um modelo personalizado para a parte inferior da página **geral** . Isso permite que você inclua controles adicionais que são exclusivos para seu aplicativo. A função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa o modelo personalizado no lugar do modelo padrão.
-   Forneça páginas de propriedades adicionais para seguir a página **geral** .
-   Forneça um objeto de retorno de chamada. Para obter mais informações, consulte [retorno de chamada do objeto para a folha de propriedades Imprimir](#callback-object-for-the-print-property-sheet).

Não é possível alterar a parte superior da página **geral** . Você não pode alterar as páginas de propriedades fornecidas pelo driver de impressora.

Para fornecer um modelo personalizado para a página Geral:

1.  Crie um modelo personalizado para a parte inferior da página **geral** modificando o modelo PRINTDLGEXORD especificado no arquivo Prnsetup. Dlg. Normalmente, o modelo personalizado deve ter o mesmo tamanho do modelo padrão. No entanto, você pode aumentar o modelo personalizado se especificar o sinalizador **PD \_ USELARGETEMPLATE** para criar uma página **geral** maior. Os identificadores de controle usados no modelo de caixa de diálogo de **impressão** padrão são definidos no arquivo Dlgs. h.
2.  Use a estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) para habilitar o modelo da seguinte maneira:
    -   Se o modelo personalizado for um recurso em um aplicativo ou em uma biblioteca de vínculo dinâmico, defina o sinalizador **PD \_ ENABLEPRINTTEMPLATE** no membro **flags** . Use os membros **HINSTANCE** e **lpPrintTemplateName** da estrutura para identificar o módulo e o nome do recurso.

        -Ou-

    -   Se o modelo personalizado já estiver na memória, defina o sinalizador **PD \_ ENABLEPRINTTEMPLATEHANDLE** . Use o membro **HINSTANCE** para identificar o objeto de memória que contém o modelo.

3.  Se você usar um modelo personalizado para definir controles adicionais, deverá fornecer um objeto de retorno de chamada para processar a entrada para seus controles. O objeto de retorno de chamada implementa um método [**IPrintDialogCallback:: HandleMessage**](/windows/win32/api/commdlg/nf-commdlg-iprintdialogcallback-handlemessage) que recebe as mensagens enviadas para a caixa de diálogo personalizada.

Para fornecer páginas de propriedades adicionais

1.  Use a função para criar as páginas adicionais.
2.  Use o membro **lphPropertyPages** da estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) para especificar uma matriz de identificadores para as páginas adicionais.

    Os procedimentos da caixa de diálogo especificados quando você criou cada página processa as mensagens enviadas para as páginas.

3.  Talvez você queira fornecer um objeto de retorno de chamada que implementa a interface. A função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) usa essa interface para passar para o aplicativo um ponteiro para uma interface [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) . Os procedimentos da caixa de diálogo para as páginas de propriedades adicionais podem usar essa interface para recuperar informações sobre a impressora selecionada no momento.

## <a name="callback-object-for-the-print-property-sheet"></a>Objeto de retorno de chamada para a folha de propriedades de impressão

Um aplicativo que exibe uma folha de propriedades de **impressão** pode implementar um objeto de retorno de chamada para receber notificações e mensagens da função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) enquanto a folha de propriedades é exibida. Para fornecer um objeto de retorno de chamada, especifique um ponteiro para o objeto no membro **lpCallback** da estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) .

O objeto de retorno de chamada deve implementar a interface [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) . A função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) chama os métodos **IPrintDialogCallback** nas seguintes situações:

-   Quando a caixa de diálogo foi inicializada
-   Quando o usuário seleciona uma impressora diferente da lista de impressoras instaladas exibida pela folha de propriedades
-   Quando ele recebe mensagens para a caixa de diálogo filho na parte inferior da página **geral** da folha de propriedades

O objeto de retorno de chamada também deve implementar a interface [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) . A função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) chama o método para passar um ponteiro para uma interface [**IPrintDialogServices**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogservices) para um aplicativo. Os métodos [**IPrintDialogCallback**](/windows/win32/api/commdlg/nn-commdlg-iprintdialogcallback) podem usar a interface **IPrintDialogServices** para recuperar informações sobre a impressora selecionada no momento. A interface **IPrintDialogServices** também é útil para aplicativos que criam páginas adicionais para seguir a página **geral** da folha de propriedades **Imprimir** . Os procedimentos da caixa de diálogo para as páginas adicionais podem chamar os métodos **IPrintDialogServices** .

 

 