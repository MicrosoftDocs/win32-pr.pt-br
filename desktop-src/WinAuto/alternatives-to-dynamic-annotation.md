---
title: Alternativas para anotação dinâmica
description: Alternativas para anotação dinâmica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0027cf9a9913efdff379d2f0c01e7bf22bc94f44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084665"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternativas para anotação dinâmica

Há outras maneiras de fornecer suporte personalizado para o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para elementos de interface do usuário e, em alguns casos, eles são a solução correta. Antes da anotação dinâmica, essas técnicas alternativas eram as únicas opções disponíveis para os desenvolvedores. Eles incluem a implementação de toda a interface **IAccessible** e técnicas programáticas.

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implementando toda a interface IAccessible

Uma técnica alternativa é implementar toda a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Essa abordagem é geralmente necessária para controles personalizados ou elementos de interface de usuário diferentes. no entanto, os custos de desenvolvimento e teste são significativos o suficiente para que sejam evitados, a menos que sejam verdadeiramente necessários. Se a meta for modificar uma única propriedade, o custo será difícil de justificar.

## <a name="programmatic-techniques"></a>Técnicas programáticas

Outra opção é usar as técnicas de subclasse e encapsulamento para modificar as informações que estão sendo expostas para uma propriedade específica. Essa é a técnica que a anotação dinâmica pretende substituir. Para substituir uma única propriedade usando a subclasse e o encapsulamento, o desenvolvedor deve executar as seguintes etapas:

1.  Subclasse a HWND do objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Interceptar a mensagem do [**WM \_ GetObject**](wm-getobject.md) para o valor correto de IParam/OBJID.
3.  Encaminhe a mensagem do [**WM \_ GetObject**](wm-getobject.md) para a classe base usando a função [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) . Se zero for retornado, chame [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); caso contrário, chame [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) no valor retornado para obter o ponteiro de interface de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo do controle.
4.  Crie uma classe wrapper, que implementa o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e encapsula o ponteiro da interface **IAccessible** retornado da etapa anterior. Essa classe wrapper envia todos os métodos e propriedades para o ponteiro da interface **IAccessible** original, exceto aqueles que devem ser substituídos. Isso envolve escrever código de encaminhamento para todas as propriedades e métodos de 21 da interface do **IAccessible** , independentemente de quantos são realmente substituídos.

Além disso, os desenvolvedores devem verificar as seguintes condições:

-   O método ou a propriedade substituído só deve manipular as IDs filho necessárias e encaminhar todas as outras para o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.
-   O encapsulamento também deve encaminhar as interfaces [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) e [**IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) somente se o objeto original oferecer suporte a elas.
-   A contagem de referência deve ser tratada corretamente, especialmente se houver suporte para outras interfaces.
-   Os valores de retorno de [**IDispatch**](idispatch-interface.md) devem ser tratados corretamente, especialmente com o método [**ITypeInfo:: Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) , que deve ser chamado com um ponteiro de interface para a interface do wrapper, não um ponteiro para a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.

Essas técnicas exigem uma quantidade considerável de trabalho, mesmo se apenas uma ou duas propriedades precisarem ser substituídas. A maior parte do código resultante se preocupa com a subclasse e o encapsulamento, e apenas uma pequena fração está, na verdade, fornecendo as informações substituídas.

No entanto, há cenários em que essas técnicas são necessárias. Por exemplo, se você estiver fazendo alterações estruturais para criar um elemento de interface do usuário de espaço reservado, deverá usar essas técnicas em vez da anotação dinâmica.

## <a name="fixing-names-derived-from-labels"></a>Corrigindo nomes derivados de rótulos

Alguns controles comuns do Microsoft Win32, como o controle caixa de edição, são quase sempre usados com um rótulo (uma entrada LTEXT no arquivo de recurso) ou uma caixa de grupo (GROUPBOX no arquivo de recurso). O Microsoft Acessibilidade Ativa deriva automaticamente a propriedade Name do controle a partir de seu rótulo. Para esses controles, o texto da janela (mostrado em Microsoft Visual Studio como a propriedade Name ou ID) é ignorado, pois geralmente é gerado automaticamente e raramente é muito descritivo; por exemplo, "IDC \_ EDIT1".

Se a interface do usuário do aplicativo não for projetada corretamente, o Microsoft Acessibilidade Ativa poderá não conseguir definir o nome corretamente. Para ser associado a um controle, a caixa rótulo ou grupo deve ser colocada imediatamente antes do controle dinâmico na ordem de tabulação.

A ordem de Tabulação pode ser alterada usando a ferramenta no Visual Studio (no menu **Formatar** quando o editor de recursos está aberto) ou editando diretamente o arquivo de recurso.

O exemplo a seguir mostra a descrição de um arquivo de recurso de uma caixa de diálogo que contém duas caixas de edição rotuladas.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
END
```



Neste exemplo, os rótulos e controles não estão listados na ordem de tabulação correta. Como resultado, o Microsoft Acessibilidade Ativa atribui o nome "Last Name" à caixa de edição First-Name e não há nenhum nome à caixa de edição Last-Name.

O exemplo a seguir mostra a listagem de recursos correta. Observe também que as teclas de atalho foram designadas nos rótulos.


```C++
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDITFIRSTNAME,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDITLASTNAME,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```



Quando os controles têm rótulos suplementares, como para valores mínimo e máximo em um TrackBar, esses rótulos devem ser colocados após o controle na ordem de tabulação. O rótulo principal do controle deve aparecer imediatamente antes do próprio controle.

## <a name="naming-controls-without-labels"></a>Controles de nomenclatura sem rótulos

Nem sempre é possível ou desejável ter um rótulo visível para cada controle. No entanto, você ainda pode fornecer um nome para o controle adicionando um rótulo invisível. Como sempre, o rótulo invisível deve preceder imediatamente o controle na ordem de tabulação.

Se você estiver usando o editor de recursos no Microsoft Visual Studio .NET, poderá definir a propriedade Visible como false. Para tornar o rótulo invisível ao editar o arquivo de recurso (. rc), adicione NOT WS \_ visível ou à parte de estilo do controle rótulo, conforme mostrado no exemplo a seguir.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Observe que qualquer tecla de atalho designada funciona mesmo que o rótulo esteja invisível.

 

 