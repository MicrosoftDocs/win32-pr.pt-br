---
title: Como criar assistentes
description: Um assistente é um tipo de folha de propriedades que fornece uma maneira simples e poderosa de orientar os usuários por meio de um procedimento.
ms.assetid: f8def159-0a68-4d7f-9840-c7b6b906ed08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fedd35bd0454e0d78ddbe74d832543e58d0a8fc7
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105762742"
---
# <a name="how-to-create-wizards"></a>Como criar assistentes

Um assistente é um tipo de folha de propriedades que fornece uma maneira simples e poderosa de orientar os usuários por meio de um procedimento.

Os assistentes são uma das chaves para simplificar a experiência do usuário. Eles permitem que você execute uma operação complexa, como a configuração de um aplicativo, e divida-o em uma série de etapas simples. Em cada ponto do processo, você pode fornecer uma explicação do que é necessário e exibir controles que permitem ao usuário fazer seleções e inserir texto.

Um assistente é, na verdade, um tipo de folha de propriedades. Uma folha de propriedades é essencialmente um contêiner para uma coleção de *páginas*, em que cada página é uma caixa de diálogo separada. Enquanto as folhas de propriedades regulares permitem que o usuário acesse qualquer página a qualquer momento, os assistentes apresentam páginas em sequência. Em vez de guias, os botões são usados para navegar para frente e para trás. A ordem na qual as páginas são exibidas é controlada pelo aplicativo e pode ser modificada com base na entrada do usuário.

Há dois estilos principais de assistente: o estilo de Wizard97 mais antigo e o estilo Aero introduzido no Windows Vista. Para ilustrações, consulte [sobre folhas de propriedades](property-sheets.md). (Um terceiro estilo, usando apenas o PSH \_ Do assistente ou \_ \_ sinalizador Lite do assistente de PSH, apresenta uma sequência simples de folhas de propriedades sem cabeçalhos ou marcas-d ' água.)

> [!Note]  
> Uma "marca d' água" no contexto de assistentes é um bitmap que aparece na margem esquerda de algumas páginas.

 

A discussão na maior parte deste documento pressupõe que você está implementando um assistente para um sistema com a [versão 5,80](common-control-versions.md) ou posterior dos controles comuns. Se você tentar usar o estilo Wizard97 com versões anteriores dos controles comuns, seu aplicativo poderá ser compilado, mas não será exibido corretamente. Para obter uma discussão sobre como criar um assistente compatível com Wizard97 em sistemas anteriores, consulte assistentes de compatibilidade retroativa mais adiante neste tópico.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="wizard-implementation"></a>Implementação do assistente

A implementação de um assistente é semelhante à implementação de uma folha de propriedades regular. No nível mais básico, é uma questão de definir um dos seguintes sinalizadores ou combinações de sinalizadores na estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) que define a folha de propriedades.



| Sinalizador                           | Estilo                                                                                                                                                 |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Assistente de PSH \_                    | Um assistente simples sem cabeçalhos ou bitmaps.                                                                                                           |
| Assistente de PSH \_ \_ Lite              | Semelhante ao assistente de PSH \_ , com algumas pequenas diferenças na aparência; por exemplo, o divisor acima dos botões é definido com a largura total da janela. |
| PSH \_ WIZARD97                  | Um assistente de Wizard97 com cabeçalhos (opcional), bitmaps de cabeçalho e marcas-d ' água.                                                                            |
| PSH \_ assistente \| PSH \_ AEROWIZARD | Um assistente de Aero. Os assistentes do Aero não usam marcas d' água ou bitmaps de cabeçalho. Eles exigem o modelo STA (single-threaded apartment).                         |



 

O procedimento básico para implementar um assistente é o seguinte:

1.  Crie um modelo de caixa de diálogo para cada página.
2.  Defina as páginas criando uma estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) para cada página. Essa estrutura define a página e contém ponteiros para o modelo de caixa de diálogo e quaisquer bitmaps ou outros recursos.
3.  Passe a estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) que foi criada na etapa anterior para a função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para criar o identificador HPROPSHEETPAGE da página.
4.  Defina o assistente criando uma estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) para ele.
5.  Passe a estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) para a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) para exibir o assistente.
6.  Implemente procedimentos de caixa de diálogo para cada página para lidar com mensagens de notificação dos controles da página e dos botões do assistente e para processar outras mensagens do Windows.

### <a name="create-the-dialog-box-templates"></a>Criar os modelos de caixa de diálogo

Há dois tipos básicos de página de assistente: exterior e interior. As páginas exteriores são as páginas de introdução (bem-vindo) e conclusão. Todos os outros são páginas interiores.

**Modelos da caixa de diálogo da página exterior**

O layout básico das páginas introdução e conclusão é idêntico. A ilustração a seguir mostra uma página de introdução Wizard97 de exemplo, com uma marca d' água de espaço reservado.

![captura de tela mostrando uma página de assistente com um gráfico à esquerda, título e corpo do texto à direita, os botões voltar, avançar e cancelar na parte inferior](images/wiz97exterior.png)

Para páginas exteriores Wizard97, o modelo de caixa de diálogo é as unidades de diálogo 317x193. Ele preenche todo o assistente, exceto a legenda e a faixa na parte inferior que contém os botões **voltar**, **Avançar** e **Cancelar** . O lado esquerdo do modelo, que é reservado para um bitmap de "marca d' água", não deve conter nenhum controle. A marca d' água é especificada na estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) do assistente e é adicionada à página automaticamente. Você deve permitir espaço para ele ao criar o modelo de recurso.

Ao criar o bitmap de marca d' água, lembre-se de que a caixa de diálogo pode aumentar em tamanho se, por exemplo, o usuário escolher uma grande fonte do sistema. Diferentes idiomas também tendem a ter diferentes métricas de fonte. Quando a página cresce, a área reservada para a marca d' água fica proporcionalmente maior. No entanto, você não pode alterar o bitmap de marca d' água, nem o bitmap é ampliado para preencher a área maior. Em vez disso, o bitmap é deixado em seu tamanho original na parte superior esquerda da área reservada. A parte da área reservada maior que não é coberta pela marca d' água é preenchida automaticamente com a cor do pixel superior esquerdo do bitmap.

Se você precisar ter bitmaps de marca d' água de tamanho diferente para métricas de fonte diferentes, duas soluções possíveis são:

-   Obtenha as métricas de fonte antes de criar o assistente e especifique um bitmap de marca d' água de tamanho adequado.
-   Não especifique um bitmap de marca d' água ao criar o assistente. Wizard97 deixará a área da marca d' água em branco. Em seguida, desenhe um bitmap de tamanho apropriado na área reservada para a marca d' água.

Você pode colocar os controles na área à direita da marca-d ' água como faria em uma caixa de diálogo comum. A cor do plano de fundo dessa área é determinada pelo sistema e não requer nenhuma ação de sua parte. Normalmente, você coloca dois controles estáticos nessa área. A parte superior contém o título e usa uma fonte grande em negrito (12 pontos Verdana negrito para Wizard97). O outro, que é para um texto explicativo, usa a fonte da caixa de diálogo padrão.

A principal diferença entre as páginas de introdução e conclusão são os botões do assistente e o texto nos controles estáticos. As páginas de introdução normalmente têm um botão **Avançar** e **voltar** , com apenas o botão **Avançar** habilitado. As páginas de conclusão têm o botão **voltar** habilitado e o botão **Avançar** é substituído por um botão **concluir** .

> [!Note]  
> Nos assistentes do Aero, o botão **voltar** é substituído por um botão de seta na barra de legenda.

 

Você pode modificar o texto no botão **concluir** enviando ao assistente uma mensagem de [**PSM \_ SETFINISHTEXT**](psm-setfinishtext.md) . Por padrão, o botão **concluir** não inclui um acelerador de teclado. Para definir um acelerador de teclado, inclua um e comercial na cadeia de texto que você passa para o PSM \_ SETFINISHTEXT. Por exemplo, "&concluir" define ' F ' como o acelerador de teclado.

**Modelos de caixa de diálogo de página interior**

As páginas interiores têm uma aparência um pouco diferente das páginas exteriores. A ilustração a seguir mostra um exemplo de página interior Wizard97, com um bitmap de cabeçalho de espaço reservado.

![captura de tela de uma página de assistente com o título e o texto do subtítulo e um gráfico na parte superior, o texto no meio e os botões na parte inferior](images/wiz97interior.png)

A área de cabeçalho na parte superior da página é manipulada pela folha de propriedades, portanto, não está incluída no modelo. O conteúdo do cabeçalho é especificado na estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) da página e na estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) do assistente. Como a página interior precisa se ajustar entre o cabeçalho e os botões, o modelo de caixa de diálogo Wizard97 é 317x143 unidades de diálogo, um pouco menor do que o modelo para páginas exteriores.

A ilustração a seguir mostra um assistente Aero criado com base no mesmo modelo.

![captura de tela que difere da anterior, tendo uma área de título na parte superior e apenas os botões Avançar e cancelar na parte inferior](images/wizardaerointerior.png)

### <a name="define-the-wizard-pages"></a>Definir as páginas do assistente

Depois de criar os modelos de caixa de diálogo e os recursos relacionados, como bitmaps e tabelas de cadeia de caracteres, você pode criar as páginas da folha de propriedades. O procedimento é semelhante ao das folhas de propriedades padrão. Primeiro, preencha os membros apropriados de uma estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) . (Alguns membros são específicos para os assistentes.) Em seguida, chame a função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para criar o identificador HPROPSHEETPAGE da página.

Os sinalizadores relacionados ao assistente a seguir podem ser definidos no membro **dwFlags** da estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) .



| Sinalizador                   | Descrição                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| PSP \_ HIDEHEADER        | Defina esse sinalizador para páginas exteriores em Wizard97. O cabeçalho não é mostrado e uma marca d' água pode ser mostrada.                                |
| PSP \_ USEHEADERTITLE    | Defina esse sinalizador para páginas interiores para colocar um título na área de cabeçalho em Wizard97 ou na parte superior da área cliente em um assistente Aero. |
| PSP \_ USEHEADERSUBTITLE | Defina esse sinalizador para páginas interiores para colocar um subtítulo na área de cabeçalho em Wizard97.                                                  |



 

Se você tiver definido PSP \_ USEHEADERTITLE ou PSP \_ USEHEADERSUBTITLE, atribua o título e o texto do subtítulo aos membros **pszHeaderTitle** e **pszHeaderSubtitle** , respectivamente. Ao atribuir cadeias de texto a membros das estruturas [**PROPSHEETPAGE**](pss-propsheetpage.md) e [**PROPSHEETHEADER**](pss-propsheetheader.md) , você pode atribuir um ponteiro de cadeia de caracteres ou usar a macro **MAKEINTRESOURCE** para atribuir um valor de um recurso de cadeia de caracteres. O recurso de cadeia de caracteres é carregado a partir do módulo especificado no membro **HINSTANCE** da estrutura **PROPSHEETHEADER** do assistente.

Quando você chama [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) para criar uma página, atribua o resultado a um elemento de uma matriz de identificadores HPROPSHEETPAGE. Essa matriz é usada ao criar a folha de propriedades. O índice de matriz do identificador de uma página determina a ordem padrão na qual ela é exibida. Depois de criar o identificador HPROPSHEETPAGE de uma página, você pode reutilizar a mesma estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) para criar a próxima página atribuindo novos valores aos membros relevantes.

Uma maneira alternativa de criar páginas é usar estruturas [**PROPSHEETPAGE**](pss-propsheetpage.md) separadas para cada página e criar uma matriz de estruturas. Essa matriz é usada em vez de uma matriz de identificadores HPROPSHEETPAGE ao criar a folha de propriedades. O uso de estruturas **PROPSHEETPAGE** separadas elimina a necessidade de chamar [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) , mas usa mais memória. Caso contrário, não há nenhuma diferença significativa entre as duas abordagens.

O exemplo a seguir define uma página Wizard97 interior atribuindo valores a uma estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) . Neste exemplo, o título da página, o subtítulo e o modelo da caixa de diálogo são todos identificados por suas IDs de recurso. Em seguida, a função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) é chamada para criar o identificador HPROPSHEETPAGE da página. Como será a segunda página a ser exibida, o identificador é atribuído à matriz de identificadores, *ahpsp*, com um índice de 1.


```C++
// g_hInstance is the global HINSTANCE of the application.
// IntPage1DlgProc is the dialog procedure for this page.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETPAGE psp = { sizeof(psp) };

psp.hInstance         = g_hInstance;
psp.dwFlags           = PSP_USEHEADERTITLE | PSP_USEHEADERSUBTITLE;
psp.lParam            = (LPARAM) &wizdata;
psp.pszHeaderTitle    = MAKEINTRESOURCE(IDS_TITLE1);
psp.pszHeaderSubTitle = MAKEINTRESOURCE(IDS_SUBTITLE1);
psp.pszTemplate       = MAKEINTRESOURCE(IDD_INTERIOR1);
psp.pfnDlgProc        = IntPage1DlgProc;

ahpsp[1] = CreatePropertySheetPage(&psp);
```



### <a name="custom-page-data"></a>Dados da página personalizada

Ao criar uma página, você pode atribuir dados personalizados a ela usando o membro **lParam** da estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) , normalmente atribuindo-lhe um ponteiro a uma estrutura definida pelo usuário.

Quando a página é selecionada pela primeira vez, o procedimento da caixa de diálogo recebe uma mensagem do [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . O valor de *lParam* da mensagem aponta para uma cópia da estrutura [**PROPSHEETPAGE**](pss-propsheetpage.md) da página, na qual você pode recuperar os dados personalizados. Você pode armazenar esses dados para uso em mensagens subsequentes usando [**SetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-setwindowlongptra) com GWL \_ UserData como o parâmetro de índice. Várias páginas podem ter um ponteiro para os mesmos dados e qualquer alteração nos dados feitas por uma página está disponível para as outras páginas em seus procedimentos de caixa de diálogo.

### <a name="define-the-wizard-property-sheet"></a>Definir a folha de propriedades do assistente

Assim como nas folhas de propriedades comuns, você define a folha de propriedades do assistente preenchendo os membros de uma estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) . Essa estrutura permite que você especifique as páginas que compõem o assistente e a ordem padrão na qual eles são exibidos, juntamente com vários parâmetros relacionados. Em seguida, inicie o assistente chamando a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) .

No estilo Wizard97, o membro **pszCaption** da estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) é ignorado. Em vez disso, o assistente exibe a legenda especificada no modelo da caixa de diálogo da página atual. Se o modelo não tem uma legenda, a legenda da página anterior é exibida. Portanto, para exibir a mesma legenda em todas as páginas, especifique a legenda no modelo para a página introdutória.

No estilo de assistente Aero, a legenda da caixa de diálogo é extraída de **pszCaption**.

Se você tiver criado uma matriz de identificadores HPROPSHEETPAGE para suas páginas, atribua a matriz ao membro **phpage** . Se, em vez disso, você tiver criado uma matriz de estruturas [**PROPSHEETPAGE**](pss-propsheetpage.md) , atribua a matriz ao membro **PPSP** e defina o \_ sinalizador PSH PROPSHEETPAGE no membro **dwFlags** .

O exemplo a seguir atribui valores a *PSH*, uma estrutura [**PROPSHEETHEADER**](pss-propsheetheader.md) e chama a função [**folha**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) para iniciar o assistente. O assistente de estilo Wizard97 tem gráficos de marca d' água e de cabeçalho, especificados por suas IDs de recurso. A matriz *ahpsp* contém todos os identificadores de HPROPSHEETPAGE e define a ordem padrão na qual eles são exibidos.


```C++
// g_hInstance is the global HINSTANCE of the application.
// ahpsp is an array of HPROPSHEETPAGE handles.

PROPSHEETHEADER psh = { sizeof(psh) };

psh.hInstance      = g_hInstance;
psh.hwndParent     = NULL;
psh.phpage         = ahpsp;
psh.dwFlags        = PSH_WIZARD97 | PSH_WATERMARK | PSH_HEADER;
psh.pszbmWatermark = MAKEINTRESOURCE(IDB_WATERMARK);
psh.pszbmHeader    = MAKEINTRESOURCE(IDB_BANNER);
psh.nStartPage     = 0;
psh.nPages         = 4;

PropertySheet(&psh);
```



### <a name="the-dialog-box-procedure"></a>O procedimento da caixa de diálogo

Cada página do assistente precisa de um procedimento de caixa de diálogo para processar mensagens do Windows, especialmente notificações de seus controles e do assistente. As três mensagens que quase todos os assistentes devem ser capazes de lidar são o [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog), o [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy)e o [**WM \_ Notify**](wm-notify.md).

A mensagem de [**\_ notificação do WM**](wm-notify.md) é recebida antes de a página ser exibida e quando um dos botões do assistente é clicado. O parâmetro *lParam* da mensagem é um ponteiro para uma estrutura de cabeçalho [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) . A ID da notificação está contida no membro do **código** da estrutura. As quatro notificações que a maioria dos assistentes precisam manipular são as seguintes.



| Código                                | Descrição                                 |
|-------------------------------------|---------------------------------------------|
| [PSN \_ SETactive](psn-setactive.md) | Enviado antes da exibição da página.          |
| [PSN \_ WIZBACK](psn-wizback.md)     | Enviado quando o botão **voltar** é clicado.   |
| [PSN \_ WIZNEXT](psn-wiznext.md)     | Enviado quando o botão **Avançar** é clicado.   |
| [PSN \_ WIZFINISH](psn-wizfinish.md) | Enviado quando o botão **concluir** é clicado. |



 

### <a name="handle-wm_initdialog-and-wm_destroy"></a>Manipule o WM \_ INITDIALOG e o WM \_ Destroy

Quando uma página está prestes a ser exibida pela primeira vez, seu procedimento de caixa de diálogo recebe uma mensagem do [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . A manipulação dessa mensagem permite que o assistente faça todas as tarefas de inicialização necessárias, como armazenar dados personalizados ou definir fontes.

Quando a folha de Propriedades for destruída, você receberá uma mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) . O assistente é destruído automaticamente pelo sistema, mas a manipulação dessa mensagem permite que você faça qualquer limpeza necessária.

### <a name="handle-psn_setactive"></a>Manipular PSN \_ SETactive

O código de notificação [PSN \_ SetActive](psn-setactive.md) é enviado cada vez que uma página está prestes a ficar visível. Na primeira vez que uma página é visitada, PSN \_ SetActive segue a mensagem [**\_ INITDIALOG do WM**](/windows/desktop/dlgbox/wm-initdialog) . Se a página for subsequentemente revisitada, ela receberá apenas uma \_ notificação SETACTIVE PSN. Normalmente, essa notificação é tratada para inicializar dados da página e habilitar os botões apropriados.

Por padrão, o assistente exibe os botões **voltar**, **Avançar** e **Cancelar** , com todos os botões habilitados. Para desabilitar um botão ou exibir **concluir** em vez de **Avançar**, você deve enviar uma mensagem de [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) . Depois que essa mensagem tiver sido enviada, o estado dos botões será preservado até ser modificado por outra mensagem de **PSM \_ SETWIZBUTTONS** , mesmo que uma nova página seja selecionada. Normalmente, todos os manipuladores [ \_ SetActive PSN](psn-setactive.md) enviam essa mensagem para garantir que cada página tenha o estado de botão correto.

Você pode alterar o estado do botão com esta mensagem a qualquer momento. Por exemplo, talvez você queira que o botão **Avançar** esteja desabilitado inicialmente. Depois que um usuário inserir todas as informações necessárias, você poderá enviar outra mensagem de [**PSM \_ SETWIZBUTTONS**](psm-setwizbuttons.md) para habilitar o botão **Avançar** e permitir que o usuário prossiga para a próxima página.

O fragmento de código a seguir usa a macro [**PropSheet \_ SetWizButtons**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setwizbuttons) para habilitar os botões **voltar** e **Avançar** em uma página interior antes de ser exibido.


```C++
case WM_NOTIFY :
    {
        LPNMHDR pnmh = (LPNMHDR)lParam;
        
        switch(pnmh->code)
        {
        
        ...
        
        case PSN_SETACTIVE :
        
            ...
            
            // This is an interior page.
            PropSheet_SetWizButtons(hwnd, PSWIZB_NEXT | PSWIZB_BACK);
            
            ...
        }
    ...
    
    }
```



### <a name="handle-psn_wiznext-psnwizback-and-psn_wizfinish"></a>Tratar PSN \_ WIZNEXT, PSNWIZBACK e PSN \_ WIZFINISH

Quando um botão **Avançar** ou **voltar** for clicado, você receberá um código de notificação [PSN \_ WIZNEXT](psn-wiznext.md) ou [PSN \_ WIZBACK](psn-wizback.md) . Por padrão, o assistente vai automaticamente para a página seguinte ou anterior na ordem que é definida quando a folha de propriedades é criada. Um motivo comum para lidar com essas notificações é impedir que o usuário alterne as páginas ou substitua a ordem de página padrão.

Para impedir que o usuário alterne as páginas, manipule a notificação do botão, chame a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor DWL MSGRESULT definido como – 1 e retorne **true**. Por exemplo:


```C++
case PSN_WIZNEXT :

        ...
        
        // Do not go to the next page yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, -1);
        
        return TRUE;
        
        ...
```



Para substituir a ordem padrão e ir para uma página específica, chame [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor DWL MSGRESULT definido como a ID de recurso da caixa de diálogo da página e retorne **true**. Por exemplo:


```C++
case PSN_WIZNEXT :

        ...
        
        // Go straight to the completion page.
        SetWindowLong(hwnd, DWL_MSGRESULT, IDD_FINISH);
        
        return TRUE;
        
        ...
```



Quando o botão **concluir** ou **Cancelar** for clicado, você receberá um código de notificação de [ \_ redefinição](psn-reset.md) de [PSN \_ WIZFINISH](psn-wizfinish.md) ou PSN, respectivamente. Quando um desses botões é clicado, o assistente é automaticamente destruído pelo sistema. No entanto, você pode lidar com essas notificações se precisar executar tarefas de limpeza antes que o assistente seja destruído. Para impedir que o assistente seja destruído quando você recebe uma \_ notificação PSN WIZFINISH, chame [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) com o \_ valor DWL MSGRESULT definido como **true** e retorne **true**. Por exemplo:


```C++
case PSN_WIZFINISH :

        ...
        
        // Not finished yet.
        SetWindowLong(hwnd, DWL_MSGRESULT, TRUE);
        
        return TRUE;
        
        ...
```



### <a name="backward-compatible-wizards"></a>Assistentes compatíveis com versões anteriores

A seção anterior pressupõe que você está implementando um assistente para um sistema com a [versão 5](common-control-versions.md) ou posterior dos controles comuns.

Se você estiver escrevendo um assistente para sistemas com versões anteriores dos controles comuns, muitos dos recursos discutidos na seção anterior não estarão disponíveis. Um número de membros das estruturas [**PROPSHEETHEADER**](pss-propsheetheader.md) e [**PROPSHEETPAGE**](pss-propsheetpage.md) usadas pelo estilo Wizard97 tem suporte apenas em controles comuns versão 5 e posteriores. No entanto, ainda é possível implementar um assistente *compatível com versões anteriores* com uma aparência semelhante à do estilo Wizard97. Para fazer isso, você deve implementar explicitamente o seguinte:

-   Adicione o gráfico de marca d' água ao modelo da caixa de diálogo para suas páginas de introdução e conclusão.
-   Faça com que todos os seus modelos tenham o mesmo tamanho. Não há nenhuma área de cabeçalho definida pelo sistema separada para páginas interiores.
-   Crie a área de cabeçalho da página interior explicitamente em seus modelos.
-   Não use um gráfico de cabeçalho porque ele pode entrar em conflito com o título ou subtítulo se o assistente alterar o tamanho.

Para obter mais informações sobre os assistentes compatíveis com versões anteriores, consulte [Assistente compatível com versões anteriores 97](/previous-versions//ms737910(v=vs.85)).

## <a name="remarks"></a>Comentários

Para obter uma discussão completa sobre problemas de design para Wizard97, consulte a [especificação Wizard97](/previous-versions//ms738248(v=vs.85)), em outro lugar na SDK do Windows. Este documento tem diretrizes para coisas como as dimensões das caixas de diálogo, dimensões e cores de bitmap e o posicionamento de controles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando folhas de propriedades](using-property-sheets.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 