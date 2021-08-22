---
title: Garantir que os elementos da interface do usuário sejam nomeados corretamente
description: Este tópico descreve a maneira correta de especificar os nomes dos elementos da interface do usuário em seus aplicativos do Microsoft Win32 para que o Microsoft Active Accessibility possa expor com precisão os nomes aos aplicativos cliente por meio do IAccessible \ 32; Propriedade name.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c047228159e011ffa9a0842f1748ee07e6af4a49ff296ae8ed65b494b8c53f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052748"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a>Garantir que os elementos da interface do usuário sejam nomeados corretamente

Este tópico descreve a maneira correta de especificar os nomes dos elementos da interface do usuário em seus aplicativos do Microsoft Win32 para que o Microsoft Active Accessibility possa expor com precisão os nomes aos aplicativos cliente por meio da propriedade [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name](name-property.md).

As informações nesta seção se Microsoft Active Accessibility somente. Ele não se aplica a aplicativos que usam o Microsoft Automação da Interface do Usuário ou aqueles baseados em linguagens de marcação, como HTML, HTML dinâmico (DHTML) ou XML.

-   [Visão geral](#overview)
-   [Como a nomeação incorreta causa problemas](#how-incorrect-naming-causes-problems)
-   [Como a MSAA obtém a propriedade name](#how-msaa-gets-the-name-property)
-   [Como encontrar e corrigir problemas de nomeação](#how-to-find-and-correct-naming-problems)
-   [Como nomear corretamente uma barra de faixa](#how-to-correctly-name-a-trackbar)
-   [Como usar rótulos invisíveis para nomear controles](#how-to-use-invisible-labels-to-name-controls)
-   [Como usar anotação direta para especificar a propriedade name](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [Etapas para anotação da propriedade Name](#steps-for-annotating-the-name-property)
    -   [Exemplo de anotação da propriedade Name](#example-of-annotating-the-name-property)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

No Microsoft Active Accessibility, cada elemento de interface do usuário em um aplicativo é representado por um objeto que expõe a interface [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Os aplicativos cliente usam as propriedades e os métodos da interface **IAccessible** para interagir com o elemento de interface do usuário e recuperar informações sobre ele. Uma das propriedades mais importantes expostas pela interface **IAccessible** é a [propriedade Name](name-property.md). Os aplicativos cliente dependem da propriedade Name para encontrar, identificar ou anunciar um elemento de interface do usuário para o usuário. Se Microsoft Active Accessibility puder expor corretamente a propriedade Name de um elemento de interface do usuário específico, os aplicativos cliente não poderão apresentar esse elemento de interface do usuário ao usuário e o elemento de interface do usuário estará inacessível a usuários com deficiências.

## <a name="how-incorrect-naming-causes-problems"></a>Como a nomeação incorreta causa problemas

Para ilustrar os problemas causados pela nomeação incorreta de elementos da interface do usuário, considere o formulário de entrada de nome mostrado na ilustração a seguir.

![ilustração de um formulário simples para inserir o nome e o sobrenome](images/incorrect-form.png)

Embora os elementos da interface do usuário no formulário pareçam ok, a implementação programática está incorreta. Para um Microsoft Active Accessibility, como um leitor de [](name-property.md) tela, a propriedade Name do controle de edição superior é "Sobrenome:" e a propriedade Name do controle de edição inferior é uma cadeia de caracteres vazia (""). O leitor de tela lerá o controle de edição superior como "Sobrenome", embora se espera que o usuário digite o nome. O leitor de tela lerá o segundo controle de edição como "sem nome", portanto, o usuário não terá ideia do que digitar no segundo controle de edição. O leitor de tela não pode ajudar o usuário a inserir dados nesse formulário simples.

Outro problema com o formulário é que nenhuma tecla de atalho é atribuída a nenhum dos controles de edição. O usuário é forçado a tabular para os controles ou usar o mouse.

As seções a seguir explicam a origem desses problemas e fornecem diretrizes para corrigi-los.

## <a name="how-msaa-gets-the-name-property"></a>Como a MSAA obtém a propriedade name

Microsoft Active Accessibility obtém a [cadeia de](name-property.md) caracteres de propriedade Name de locais diferentes, dependendo do tipo do elemento de interface do usuário. Para a maioria dos elementos da interface do usuário que têm texto de janela associado, Microsoft Active Accessibility o texto da janela como a cadeia de caracteres da propriedade Name. Exemplos desse tipo de elemento de interface do usuário incluem controles como botões, itens de menu e dicas de ferramenta.

Para os controles a seguir, Microsoft Active Accessibility ignora o texto da janela e, em vez disso, procura um rótulo de texto estático (ou rótulo de caixa de grupo) imediatamente antes do controle na ordem de tabulação.

-   Caixas de combinação
-   Seladores de data e hora
-   Editar e editar controles rich edit
-   Controles de endereço IP
-   Caixas de listagem
-   Listar exibições
-   Barras de progresso
-   Scrollbars
-   Controles estáticos que têm o \_ estilo SS ICON ou SS \_ BITMAP
-   Trackbars
-   Exibições de árvore

Se os controles anteriores não são acompanhados por rótulos de texto estático ou se os rótulos não são implementados corretamente, Microsoft Active Accessibility não poderá fornecer a propriedade [Name](name-property.md) correta para aplicativos cliente.

A maioria dos controles anteriores realmente tem texto de janela associado. O editor de recursos gera automaticamente o texto da janela, que consiste em uma cadeia de caracteres genérica, como "edit1" ou "listbox3". Embora os desenvolvedores possam substituir o texto da janela gerado por um texto mais significativo, a maioria nunca substitui. Como o texto da janela gerado não tem nenhum significado para o usuário, Microsoft Active Accessibility o ignora e usa o rótulo de texto estático que o acompanha.

## <a name="how-to-find-and-correct-naming-problems"></a>Como encontrar e corrigir problemas de nomeação

No formulário de entrada de nome mostrado em How Incorrect Noming Cause Problems, a causa dos problemas é que a ordem de tabulação dos controles está incorreta. Examinar a interface do usuário com uma ferramenta de teste como [Inspecionar](inspect-objects.md) revelaria os problemas com a hierarquia de objetos. A captura de tela a seguir mostra a hierarquia de objetos quebrada do formulário de entrada de nome como aparece em Inspecionar.

![captura de tela da ferramenta de inspeção mostrando uma hierarquia de objetos incorreta do formulário de entrada de nome](images/incorrect-object-hierarchy.png)

Na captura de tela anterior, observe que a hierarquia de objetos não combina com a estrutura dos controles conforme eles aparecem na interface do usuário do formulário de entrada de nome. Observe também que [Inspecionar](inspect-objects.md) atribuiu o nome incorreto ao próximo ao último item (é o controle de edição para inserir o primeiro nome e deve ser um chamado "Nome:". Por fim, observe que Inspecionar não pôde encontrar um nome para o último item (é o controle de edição para inserir o sobrenome e deve ter um nome de "Sobrenome:".

O exemplo a seguir mostra o conteúdo do arquivo de recurso para o formulário de entrada de nome. Observe que a ordem de tabulação não é consistente com a estrutura lógica dos controles conforme eles aparecem na interface do usuário. Observe também que nenhuma tecla de atalho é especificada para os dois controles de edição.

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

Para corrigir os problemas com o formulário de entrada de nome, o arquivo de recurso (.rc) deve ser editado para especificar atalhos de teclado e os controles devem ser colocados na seguinte ordem:

1.  O rótulo de texto estático "&Nome:".
2.  O controle de edição para inserir o nome (IDC \_ EDIT1).
3.  O rótulo de texto estático "&Sobrenome:".
4.  O controle de edição para inserir o sobrenome (IDC \_ EDIT2).
5.  O botão de push padrão "OK".

O exemplo a seguir mostra o arquivo de recurso corrigido para o formulário de entrada de nome:

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

Para fazer correções em um arquivo de recurso, você pode editar o arquivo diretamente ou pode usar a ferramenta Ordem de Tabulação Microsoft Visual Studio. Você pode acessar a ferramenta Ordem de Tabulação Visual Studio pressionando CTRL+D ou selecionando **Ordem** de Tabulação **no** menu Formatar.

Depois de corrigir e recriar o aplicativo, a interface do usuário do formulário de entrada de nomes terá a mesma aparência de antes. No entanto, Microsoft Active Accessibility agora fornecerá as propriedades de Nome corretas para aplicativos cliente e definirá o foco corretamente quando o usuário pressionar os atalhos de teclado ALT+F ou ALT+L. Além disso, [Inspecionar](inspect-objects.md) mostrará a hierarquia de objetos correta, como mostra a captura de tela a seguir.

![captura de tela da ferramenta de explorador acessível mostrando uma hierarquia de objetos correta do formulário de entrada de nome](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a>Como nomear corretamente uma barra de faixa

Ao definir uma barra de faixa (ou controle deslizante), verifique se o rótulo de texto estático principal para a barra de faixa aparece antes da barra de faixa e se os rótulos de texto estático para os intervalos mínimo e máximo aparecem após a barra de faixa. Lembre-se Microsoft Active Accessibility usa o rótulo de texto estático que precede imediatamente um controle como a [propriedade Name](name-property.md) para o controle. Colocar o rótulo de texto estático principal imediatamente antes da barra de faixa e os outros rótulos depois dela garante que Microsoft Active Accessibility a propriedade Name correta para um cliente.

A ilustração a seguir mostra uma barra de faixa típica com um rótulo de texto estático principal chamado "Velocidade" e rótulos de texto estático para os intervalos mínimo ("min") e máximo ("max").

![ilustração de um controle de barra de faixa que tem um rótulo principal e rótulos para os intervalos mínimo e máximo](images/speed-trackbar.png)

O exemplo a seguir mostra a maneira correta de definir uma barra de faixa e seus rótulos de texto estático no arquivo de recurso:

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a>Como usar rótulos invisíveis para nomear controles

Nem sempre é possível ou desejável ter um rótulo visível para cada controle. Por exemplo, às vezes, adicionar rótulos pode causar alterações indesejáveis na aparência da interface do usuário. Nesse caso, você pode usar rótulos invisíveis. Microsoft Active Accessibility ainda escolherá o texto associado a um rótulo invisível, mas o rótulo não aparecerá nem interferirá na interface do usuário visual.

Assim como com rótulos visíveis, um rótulo invisível deve preceder imediatamente o controle na ordem de tabulação. Para tornar um rótulo invisível em um arquivo de recurso (.rc), adicione ou à parte de estilo `NOT WS_VISIBLE` do controle de texto `|~WS_VISIBLE` estático. Se você estiver usando o Editor de Recursos Visual Studio, poderá definir a propriedade Visible como False.

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a>Como usar anotação direta para especificar a propriedade name

Os proxies padrão incluídos no componente Microsoft Active Accessibility runtime do Oleacc.dll, Oleacc.dll, fornecem automaticamente um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para todos os controles Windows padrão. Se você personalizar um controle Windows padrão, os proxies padrão fazem o melhor para fornecer com precisão todas as propriedades **IAccessible** para seu controle personalizado. Você deve testar completamente um controle personalizado para garantir que os proxies padrão estão fornecendo valores de propriedade precisos e completos. Se o teste revelar valores de propriedade imprecisos ou incompletos, você poderá usar a técnica de Anotação Dinâmica chamada anotação direta para fornecer valores de propriedade corretos e adicionar os que estão ausentes.

Observe que a Anotação Dinâmica não é apenas para controles com suporte pelos Microsoft Active Accessibility proxies. Você também pode usá-lo para modificar ou fornecer propriedades para qualquer controle que forneça sua própria implementação [**de IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Esta seção se concentra em usar a anotação direta para fornecer um valor correto para a [Propriedade Name](name-property.md) do objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um controle. Você também pode usar a anotação direta para fornecer outros valores de propriedades. Além disso, outras técnicas de anotação dinâmica ao lado da anotação direta estão disponíveis, e os recursos e funcionalidades da API de anotação dinâmica se estendem muito além do que é descrito nesta seção. Para obter mais informações sobre a anotação dinâmica, consulte [API de anotação dinâmica](dynamic-annotation-api.md).

### <a name="steps-for-annotating-the-name-property"></a>Etapas para anotar a propriedade Name

Usar a anotação direta para alterar a [Propriedade Name](name-property.md) de um controle envolve as etapas a seguir.

1.  Inclua os seguintes arquivos de cabeçalho:
    -   Initguid. h
    -   OleAcc. h

    > [!Note]  
    > Para definir GUIDs, você deve incluir Initguid. h antes de OleAcc. h no mesmo arquivo.

     

2.  Inicialize a biblioteca de Component Object Model (COM) chamando a função [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) , normalmente durante o processo de inicialização do aplicativo.
3.  Logo após a criação do controle de destino (normalmente durante a mensagem [ \_ INITDIALOG do WM](../dlgbox/wm-initdialog.md) ), crie uma instância do Gerenciador de anotações e obtenha um ponteiro para o ponteiro [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
4.  Anote a [Propriedade Name](name-property.md) do controle de destino usando o método [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) .

5.  Libere o ponteiro [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
6.  Antes de o controle de destino ser destruído (normalmente ao manipular a mensagem de [ \_ destruição do WM](../winmsg/wm-destroy.md) ), crie uma instância do Gerenciador de anotações e obtenha um ponteiro para sua interface [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
7.  Use o método [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) para limpar as anotações de [propriedade de nome](name-property.md) do controle de destino.
8.  Libere o ponteiro [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
9.  Antes de o aplicativo sair (normalmente durante o processamento da mensagem do [WM \_ Destroy](../winmsg/wm-destroy.md) ), libere a biblioteca com chamando a função [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .

A função [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) usa cinco parâmetros. Os três primeiros —*HWND*, *idObject* e *idChild*— combinam para identificar o controle. O quarto parâmetro, *idProp*, especifica o identificador da propriedade a ser alterada. Para alterar a [Propriedade Name](name-property.md), defina *idProp* como **Propid \_ ACC \_ Name**. (Para obter uma lista de outras propriedades que podem ser definidas por meio da anotação direta, consulte [usando anotação direta](using-direct-annotation.md).) O último parâmetro de **SetHwndPropStr**, *Str*, é a nova cadeia de caracteres a ser usada como a propriedade Name.

### <a name="example-of-annotating-the-name-property"></a>Exemplo de anotação da propriedade Name

O código de exemplo a seguir mostra como usar a anotação direta para alterar a [Propriedade Name](name-property.md) do objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um controle. Para simplificar as coisas, o exemplo usa uma cadeia de caracteres embutida em código ("novo nome do controle") para definir a propriedade Name. As cadeias de caracteres embutidas em código não devem ser usadas na versão final do seu aplicativo porque não podem ser localizadas. Em vez disso, sempre carregue as cadeias de caracteres do arquivo de recursos. Além disso, o exemplo não mostra as chamadas para as funções [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[API de anotação dinâmica](dynamic-annotation-api.md)
</dt> <dt>

[Fornecendo a propriedade Name](providing-the-name-property.md)
</dt> <dt>

[Ferramentas de teste](testing-tools.md)
</dt> </dl>

 

 