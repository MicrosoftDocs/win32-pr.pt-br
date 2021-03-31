---
title: Active Directory folhas de propriedades de usuários e computadores
description: O snap-in Active Directory usuários e computadores do MMC foi projetado para exibir uma folha de propriedades para vários objetos em um servidor Active Directory.
ms.assetid: 38032d89-9549-475c-90aa-dac5cfe11084
ms.tgt_platform: multiple
keywords:
- Active Directory folhas de propriedades de usuários e computadores AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea24f34e86f21af178e975852accb667bb69e4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640441"
---
# <a name="active-directory-users-and-computers-property-sheets"></a>Active Directory folhas de propriedades de usuários e computadores

O snap-in Active Directory usuários e computadores do MMC foi projetado para exibir uma folha de propriedades para vários objetos em um servidor Active Directory. A folha de propriedades contém uma ou mais páginas que são usadas para exibir e modificar dados de objeto. Diferentes tipos de objeto têm conjuntos diferentes de páginas exibidas para eles. O snap-in Active Directory usuários e computadores do MMC também permite que fornecedores de terceiros adicionem páginas personalizadas à folha de propriedades para um tipo específico de objeto. Para obter mais informações, consulte [páginas de propriedades para uso com especificadores de exibição](property-pages-for-use-with-display-specifiers.md).

Alguns aplicativos, além do snap-in Active Directory usuários e computadores do MMC, devem fornecer ao usuário o modo de exibição de capacidade e editar os atributos de um objeto em um servidor Active Directory. O aplicativo poderia implementar suas próprias folhas de propriedades, mas é melhor oferecer uma interface de usuário consistente para reduzir a confusão e o tempo de aprendizagem. Felizmente, o snap-in do MMC Active Directory usuários e computadores permite que qualquer aplicativo COM OLE exiba uma folha de propriedades para um objeto que seja idêntico à folha de propriedades que seria exibida pelo snap-in do MMC Active Directory usuários e computadores para o mesmo objeto.

Para obter mais informações e um exemplo de código que hospeda uma folha de propriedades usuários e computadores Active Directory, consulte o exemplo PropSheetHost no SDK (Software Development Kit) da plataforma.

## <a name="developer-audience"></a>Público do desenvolvedor

Esta documentação pressupõe que o leitor esteja familiarizado com a operação COM e o desenvolvimento de componentes usando o C++. Atualmente, não é possível criar uma extensão de folha de propriedades Active Directory usando Visual Basic.

## <a name="hosting-an-active-directory-users-and-computers-property-sheet"></a>Como hospedar uma folha de propriedades de usuários e computadores Active Directory

**Para exibir uma folha de propriedades para um objeto em um servidor de Active Directory**

1.  Crie uma janela que possa ser usada para processar mensagens. Isso pode ser uma janela existente ou uma janela de finalidade especial. Isso é conhecido como a *janela oculta*.
2.  Crie um objeto OLE COM derivado de [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject). Este objeto de dados deve dar suporte aos seguintes formatos de dados:

    -   [**CFSTR \_ DSOBJECTNAMES**](cfstr-dsobjectnames.md) esse formato de dados contém um [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) que identifica o objeto ao qual a folha de propriedades se aplica. Ao hospedar uma folha de propriedades, os membros mais significativos da estrutura **DSOBJECTNAMES** são mostrados na lista a seguir.

        **clsidNamespace** Reservado. Defina isso para um GUID para seu aplicativo aqui caso ele seja usado no futuro.
        
        **aObjects** Contém uma matriz de estruturas [**DSBOJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Cada estrutura **DSBOJECT** representa um único objeto de diretório. O membro **cItems** contém o número de elementos na matriz. Somente o primeiro objeto nessa matriz é usado. Outros objetos são ignorados.

    -   [**CFSTR \_ DSDISPLAYSPECOPTIONS**](cfstr-ds-display-spec-options.md) esse formato de dados contém uma estrutura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) que contém dados que serão usados pelas páginas de propriedades, como para onde carregar as páginas de propriedades, o servidor e as credenciais a serem usadas e assim por diante. Os membros mais significativos do **DSDISPLAYSPECOPTIONS** são mostrados na lista a seguir.

        **offsetAttribPrefix** A cadeia de caracteres de prefixo de atributo determina onde a lista de páginas de propriedades é obtida. Isso deve conter uma das cadeias de caracteres a seguir.

        

        | Cadeia de prefixo de atributo | Descrição                                              |
        |-------------------------|----------------------------------------------------------------------------------------------------------------------|
        | ADM<br/>      | As páginas de propriedades são carregadas do atributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) .<br/> |
        | Shell<br/>      | As páginas de propriedades são carregadas do atributo [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) .<br/> |

        


    -   [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) este formato de dados contém uma estrutura [**PROPSHEETCFG**](propsheetcfg.md) que contém dados de host da folha de propriedades. Ao hospedar uma folha de propriedades, os membros mais significativos da estrutura **PROPSHEETCFG** contêm os dados mostrados na lista a seguir.

        **lNotifyHandle** Deve ser zero.
        **hwndParentSheet**  Contém o identificador da janela para receber mensagens [**de \_ \_ \_ alteração de notificação do WM ADSPROP**](wm-adsprop-notify-change.md) quando algo em uma das páginas é alterado e é aplicado. Pode ser **NULL** se esta mensagem não for desejada.

        **hwndHidden** Contém o identificador da janela para receber o [**WM \_ DSA \_ folha \_ criar \_ notificação**](wm-dsa-sheet-create-notify.md) e o [**WM \_ DSA \_ folha \_ fechar \_ notificar**](wm-dsa-sheet-close-notify.md) mensagens. Defina isso para o identificador da janela oculta.

        **wParamSheetClose** Contém um identificador definido pelo aplicativo que é retornado no *wParam* na [**\_ folha DSA do WM \_ \_ fechar \_**](wm-dsa-sheet-close-notify.md) mensagem de notificação. Se esse membro for zero, a mensagem de **\_ notificação de \_ \_ fechamento \_ da folha DSA do WM** não será postada na janela oculta.


3.  Crie uma instância do objeto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) e obtenha a interface [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) para o objeto. Também é possível duplicar o comportamento do objeto **CLSID \_ DsPropertyPages** . Para obter mais informações, consulte duplicando o comportamento do \_ objeto CLSID DsPropertyPages.
4.  Inicialize o objeto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) chamando o método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . Os parâmetros *pidlFolder* e *hkeyProgID* não são usados neste método. O parâmetro *pdtobj* é o ponteiro para o objeto de dados criado na etapa 2. Quando o método **IShellExtInit:: Initialize** for chamado, o objeto **CLSID \_ DsPropertyPages** salvará uma referência ao objeto de dados.
5.  Obtenha a interface [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) para o objeto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) e chame o método [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) . O parâmetro *lpfnAddPage* é o endereço de uma função de retorno de chamada que você deve implementar. O formato dessa função é mostrado abaixo. Se a função de retorno de chamada for declarada como um membro de uma classe C++, a função de retorno de chamada deverá ser declarada como **estática**. O parâmetro *lParam* é um valor definido pelo aplicativo que pode ser usado para identificar o objeto que implementa a função de retorno de chamada. Quando o método **IShellPropSheetExt:: AddPages** for chamado, o objeto **CLSID \_ DsPropertyPages** obterá os dados do objeto de dados e enumerará as páginas de propriedades registradas para os especificadores de exibição de objeto. O objeto **CLSID \_ DsPropertyPages** enumerará os objetos da página de propriedades, chamando o método **IShellPropSheetExt:: AddPages** de cada objeto.

    ```C++
    BOOL CALLBACK AddPagesCallback(HPROPSHEETPAGE, LPARAM)
    ```

    

6.  Cada página adicionada pelos objetos da página de propriedades resultará na chamada da sua função de retorno com o identificador para a página de propriedades e o valor definido pelo aplicativo. Sua função de retorno de chamada deve armazenar cada identificador de página de propriedade que é passado. Quando o método [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) do objeto [**\_ DsPropertyPages do CLSID**](guids-of-user-interface-elements.md) for retornado, todas as páginas terão sido adicionadas por meio de sua função de retorno de chamada.
7.  Preencha uma estrutura [**PROPSHEETHEADER**](/windows/win32/api/prsht/ns-prsht-propsheetheadera_v2) para exibir a folha de propriedades. O membro **phpage** recebe um ponteiro para uma matriz de identificadores de página que foram coletados pela função de retorno de chamada. O membro **nPages** recebe o número de páginas na matriz de identificadores de página.
8.  Exiba a folha de propriedades chamando a função [**folha**](/windows/win32/api/prsht/nf-prsht-propertysheeta) .

Se os dados em qualquer página forem alterados e os botões **OK** ou **aplicar** forem clicados, a janela identificada pelo membro **hwndParentSheet** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) receberá uma mensagem de [**\_ \_ \_ alteração de notificação do WM ADSPROP**](wm-adsprop-notify-change.md) . Essa mensagem é estritamente uma notificação e não requer nenhuma ação específica.

Quando a página for fechada, a janela identificada pelo membro **hwndHidden** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) receberá uma mensagem [**de \_ \_ notificação de \_ fechamento \_ da folha DSA do WM**](wm-dsa-sheet-close-notify.md) . Essa mensagem é estritamente uma notificação e não requer nenhuma ação específica a ser executada.

Em alguns casos, as folhas de propriedades existentes precisarão exibir uma folha de propriedades secundária. Por exemplo, se você exibir a folha de propriedades de um objeto de usuário e selecionar o **membro da** página, uma lista de grupos dos quais o usuário é membro será exibida. Se você clicar duas vezes em um desses grupos na lista, a folha de propriedades desse grupo será exibida. A folha de propriedades primária não exibe a planilha secundária por si só. Ele solicita que o host exiba a planilha secundária enviando uma folha de dados do [**WM \_ DSA \_ \_ criar \_ notificação**](wm-dsa-sheet-create-notify.md) para a janela identificada pelo membro **hwndHidden** da estrutura [**PROPSHEETCFG**](propsheetcfg.md) . O *wParam* da **folha do DSA do WM \_ \_ \_ criar \_ notificação** é um ponteiro para uma estrutura de [**\_ \_ \_ informações da página DSA s**](dsa-sec-page-info.md) que contém informações sobre a folha de propriedades secundária e o objeto que ela representa. Em resposta a essa mensagem, o host da folha de propriedades deve exibir a folha de propriedades secundária da mesma maneira que mostrado acima. Depois de processar a mensagem de **notificação de \_ \_ \_ criação \_ da folha DSA do WM** , o receptor da mensagem deve liberar a estrutura de **\_ \_ \_ informações da página DSA s** , passando o valor *wParam* para a função [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

## <a name="duplicating-the-behavior-of-the-clsid_dspropertypages-object"></a>Duplicando o comportamento do objeto CLSID \_ DsPropertyPages

**Para duplicar o comportamento do \_ objeto CLSID DsPropertyPages**

1.  Enumere os valores no atributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) ou [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) para o especificador de exibição para a classe de objeto. Cada valor é uma cadeia de caracteres que contém um número, seguido por uma vírgula, seguida pela representação da cadeia de caracteres do identificador de classe da extensão da página de propriedades. Para obter mais informações sobre o formato das páginas de propriedades exibir valores de especificador, consulte [registrando o objeto com da página de propriedades em um especificador de exibição](registering-the-property-page-com-object-in-a-display-specifier.md).
2.  Converta cada cadeia de caracteres de identificador de classe em um **CLSID** usando a função [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .
3.  Classifique os identificadores de classe de extensão pelo número que precede cada cadeia de caracteres de identificador de classe no valor do atributo. Se dois números forem idênticos, classifique os identificadores de classe na ordem em que os valores de atributo são obtidos do servidor de Active Directory.
4.  Enumere os identificadores de classe de extensão, criando uma instância de cada extensão.
5.  Para cada extensão, na ordem classificada acima, chame o [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) da extensão com as mesmas informações descritas na etapa 4 do procedimento de folha de propriedades usuários e computadores de Active Directory hospedagem.
6.  Para cada extensão, na ordem classificada acima, chame as [**paginações IShellPropSheetExt::**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) addda extensão com as mesmas informações descritas na etapa 5 do procedimento de folha de propriedades usuários e computadores Active Directory de hospedagem.

Se possível, use o objeto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) para criar as páginas em vez de fazer isso manualmente. O **CLSID \_ DsPropertyPages** foi otimizado e manipulará corretamente os casos de falha, como quando nenhum especificador de exibição está disponível para a localidade atual. Além disso, o objeto **CLSID \_ DsPropertyPages** pode mudar no futuro, o que significa que suas folhas de propriedades podem não corresponder exatamente às exibidas pelo snap-in do MMC Active Directory usuários e computadores.

## <a name="special-programming-elements"></a>Elementos de programação especiais

Atualmente, os seguintes elementos de programação não estão definidos em um arquivo de cabeçalho publicado. Para usar esses elementos, você mesmo deve defini-los no formato exato mostrado na página de referência específica.

-   [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
-   [**PROPSHEETCFG**](propsheetcfg.md)
-   [**\_notificação de \_ fechamento da folha DSA \_ do WM \_**](wm-dsa-sheet-close-notify.md)
-   [**\_notificação de \_ criação da folha DSA \_ do WM \_**](wm-dsa-sheet-create-notify.md)
-   [**\_ \_ informações da página DSA SEC \_**](dsa-sec-page-info.md)

## <a name="example-code"></a>Código de exemplo

O exemplo de código C++ a seguir mostra uma maneira segura de definir esses elementos que continuarão a funcionar mesmo que esses elementos sejam definidos em um arquivo de cabeçalho publicado no futuro.


```C++
#ifndef CFSTR_DS_PROPSHEETCONFIG
    #define CFSTR_DS_PROPSHEETCONFIG_W L"DsPropSheetCfgClipFormat"
    #define CFSTR_DS_PROPSHEETCONFIG_A "DsPropSheetCfgClipFormat"

    #ifdef UNICODE
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_W
    #else
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_A
    #endif //UNICODE
#endif //CFSTR_DS_PROPSHEETCONFIG


#ifndef WM_ADSPROP_SHEET_CREATE
    #define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
#endif


#ifndef WM_DSA_SHEET_CREATE_NOTIFY
    #define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
#endif


#ifndef WM_DSA_SHEET_CLOSE_NOTIFY
    #define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5) 
#endif


#ifndef DSA_SEC_PAGE_INFO
    typedef struct _DSA_SEC_PAGE_INFO
    {
        HWND    hwndParentSheet;
        DWORD   offsetTitle;
        DSOBJECTNAMES dsObjectNames;
    } DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
#endif //DSA_SEC_PAGE_INFO

#ifndef PROPSHEETCFG
    typedef struct _PROPSHEETCFG
    {  
        LONG_PTR lNotifyHandle;  
        HWND hwndParentSheet;  
        HWND hwndHidden;  
        WPARAM wParamSheetClose;
    } PROPSHEETCFG, *PPROPSHEETCFG;
#endif //PROPSHEETCFG
```



 

