---
title: Alternativas à Anotação Dinâmica
description: Alternativas à Anotação Dinâmica
ms.assetid: d8019c65-620b-4aa2-a631-cc32f34e5510
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af7582ec0fa3f317a0fabbdde0474c6a2e4d0b361062243d7518edf317477ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122426"
---
# <a name="alternatives-to-dynamic-annotation"></a>Alternativas à Anotação Dinâmica

Há outras maneiras de fornecer suporte personalizado de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para elementos de interface do usuário e, em alguns casos, eles são a solução correta. Antes da Anotação Dinâmica, essas técnicas alternativas eram as únicas opções disponíveis para desenvolvedores. Eles incluem a implementação de todas as técnicas programáticas e interface **IAccessible.**

## <a name="implementing-all-of-the-iaccessible-interface"></a>Implementando toda a interface IAccessible

Uma técnica alternativa é implementar toda a interface [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Essa abordagem geralmente é necessária para controles personalizados ou elementos de interface do usuário radicalmente diferentes; no entanto, os custos de desenvolvimento e teste são significativos o suficiente para que eles devem ser evitados, a menos que realmente necessário. Se a meta for modificar uma única propriedade, o custo será difícil de justificar.

## <a name="programmatic-techniques"></a>Técnicas programáticas

Outra opção é usar técnicas de subclasse e de empacotamento para modificar as informações que estão sendo expostas para uma propriedade específica. Essa é a técnica que a Anotação Dinâmica se destina a substituir. Para substituir uma única propriedade usando a subclasse e o empacotamento, o desenvolvedor deve executar as seguintes etapas:

1.  Subclasse o HWND do [**objeto IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
2.  Intercepte [**a mensagem WM \_ GETOBJECT**](wm-getobject.md) para o valor IParam/OBJID correto.
3.  Encaminhe [**a mensagem WM \_ GETOBJECT**](wm-getobject.md) para a classe base usando a [*função CallWndProc.*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) Se zero for retornado, chame [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject); caso contrário, [**chame LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) no valor retornado para obter o ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo do controle.
4.  Crie uma classe wrapper, que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e envolve o ponteiro da interface **IAccessible** retornado da etapa anterior. Essa classe wrapper envia todos os métodos e propriedades para o ponteiro de interface **IAccessible** original, exceto aqueles que devem ser substituídos. Isso envolve escrever código de encaminhamento para todas as 21 propriedades e métodos da interface **IAccessible,** independentemente de quantos realmente são substituídos.

Além disso, os desenvolvedores devem verificar as seguintes condições:

-   O método ou a propriedade substituído só deve manipular as IDs filho necessárias e encaminhar todas as outras para o ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.
-   O empacotamento também deve encaminhar as interfaces [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) [**e IOleWindow**](/windows/desktop/api/oleidl/nn-oleidl-iolewindow) somente se o objeto original dá suporte a elas.
-   A contagem de referência deve ser tratada corretamente, especialmente se há suporte para outras interfaces.
-   Os valores de retorno de [**IDispatch**](idispatch-interface.md) devem ser tratados corretamente, especialmente com o método [**ITypeInfo::Invoke,**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypeinfo-invoke) que deve ser chamado com um ponteiro de interface para a interface wrapper, não um ponteiro para a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original.

Essas técnicas exigem uma quantidade considerável de trabalho, mesmo que apenas uma ou duas propriedades precisem ser substituídos. A maioria do código resultante se preocupa com a subclasse e o empacotamento, e apenas uma pequena fração está, na verdade, fornecendo as informações substituídos.

No entanto, há cenários em que essas técnicas são necessárias. Por exemplo, se você estiver fazendo alterações estruturais para criar um elemento de interface do usuário de espaço reservado, deverá usar essas técnicas em vez de Anotação Dinâmica.

## <a name="fixing-names-derived-from-labels"></a>Corrigindo nomes derivados de rótulos

Alguns controles comuns do Microsoft Win32, como o controle de caixa de edição, quase sempre são usados com um rótulo (uma entrada LTEXT no arquivo de recurso) ou uma caixa de grupo (GROUPBOX no arquivo de recurso). Microsoft Active Accessibility deriva automaticamente a propriedade name do controle de seu rótulo. Para esses controles, o texto da janela (mostrado em Microsoft Visual Studio como a propriedade Nome ou ID) é ignorado, pois geralmente é gerado automaticamente e raramente é muito descritivo; por exemplo, "IDC \_ EDIT1".

Se a interface do usuário do aplicativo não for projetada corretamente, Microsoft Active Accessibility poderá não conseguir definir o nome corretamente. Para ser associado a um controle, a caixa rótulo ou grupo deve ser colocada imediatamente antes do controle dinâmico na ordem de tabulação.

A ordem de tabulação pode ser alterada usando a ferramenta no Visual Studio (no **menu** Formatar quando o editor de recursos estiver aberto) ou editando diretamente o arquivo de recurso.

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



Neste exemplo, os rótulos e os controles não estão listados na ordem de tabulação correta. Como resultado, Microsoft Active Accessibility atribui o nome "Sobrenome" à caixa de edição de nome e nenhum nome à caixa de edição de sobrenome.

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



Quando os controles têm rótulos suplementares, como para valores mínimos e máximos em uma barra de faixa, esses rótulos devem ser colocados após o controle na ordem de tabulação. O rótulo principal do controle deve aparecer imediatamente antes do próprio controle.

## <a name="naming-controls-without-labels"></a>Controles de nomeação sem rótulos

Nem sempre é possível ou desejável ter um rótulo visível para cada controle. No entanto, você ainda pode fornecer um nome para o controle adicionando um rótulo invisível. Como sempre, o rótulo invisível deve preceder imediatamente o controle na ordem de tabulação.

Se você estiver usando o Editor de Recursos Microsoft Visual Studio .NET, poderá definir a propriedade Visible como False. Para tornar o rótulo invisível ao editar o arquivo de recurso (.rc), adicione NOT WS VISIBLE ou à parte de estilo do controle de rótulo, conforme mostrado \_ no exemplo a seguir.


```C++
    LTEXT           "&FullName:",IDC_STATIC,111,23,44,8,NOT WS_VISIBLE
```



Observe que qualquer tecla de atalho designada funciona mesmo que o rótulo seja invisível.

 

 