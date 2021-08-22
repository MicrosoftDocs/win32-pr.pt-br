---
title: Como as IDs filho são usadas em parâmetros
description: Este tópico descreve parâmetros de entrada, parâmetros de saída e casos especiais para interpretar IDs filho retornadas dos métodos IAccessible.
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc0c3be970fb4a688a0a5447b72719428e78e074cbc7a17f2b6b698fcca177f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052714"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Como as IDs filho são usadas em parâmetros

Este tópico descreve parâmetros de entrada, parâmetros de saída e casos especiais para interpretar IDs filho retornadas dos métodos [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

## <a name="input-parameters"></a>Parâmetros de Entrada

Muitas das funções Microsoft Active Accessibility e a maioria das [**propriedades IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) levam uma [**estrutura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) como um parâmetro de entrada. Para a maioria das **propriedades IAccessible,** esse parâmetro permite que os desenvolvedores cliente especifiquem se querem informações sobre o próprio objeto ou sobre um dos elementos simples do objeto.

Microsoft Active Accessibility fornece a CONSTANTE **CHILDID \_ SELF** para indicar que as informações são necessárias sobre o próprio objeto. Para obter informações sobre um elemento simples, os desenvolvedores cliente especificam sua ID filho no [**parâmetro VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant)

Ao inicializar um parâmetro [**VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) especifique **vT \_ I4** no membro **vt,** além de especificar o valor da ID filho (ou **CHILDID \_ SELF**) no membro **lVal.**

Por exemplo, para obter o nome de um objeto e não um dos elementos filho do objeto, inicialize [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) para o primeiro parâmetro de [**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **CHILDID \_ SELF** no membro **lVal** e **VT \_ I4** no membro **vt)** e, em seguida, chame **IAccessible::get \_ accName**.

## <a name="output-parameters"></a>Parâmetros de saída

Várias funções e métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) têm um parâmetro de saída [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) que contém uma ID filho ou um ponteiro de \* interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) para um objeto filho. Há diferentes etapas que um cliente deve seguir, dependendo de receber uma ID filho **VT \_ I4** (elemento simples) ou um ponteiro de interface **IDispatch** com **CHILDID \_ SELF** (objeto completo). Seguir estas etapas fornecerá um ponteiro de interface **IAccessible** e uma ID filho que, juntos, permitem que os clientes usem os métodos e propriedades **IAccessible.** Essas etapas se aplicam aos métodos [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest), [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)e [**get \_ accSelection.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) Eles também se aplicam às funções de cliente [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)e [**AccessibleObjectFromWindow.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)

A tabela a seguir lista o possível resultado retornado e as etapas de pós-processamento necessárias para que os clientes tenham um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e uma ID filho.



| Resultado retornado                                      | Pós-processamento para o valor de retorno                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ponteiro da interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) | Esse é um objeto completo. Chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para acessar o ponteiro da interface [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)<br/> Use o ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com **CHILDID \_ SELF** para acessar métodos e propriedades **IAccessible.**<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_ID filho da VT I4                                      | Chame [**IAccessible::get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) usando a ID filho para ver se você tem um ponteiro de interface [**IDispatch.**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) Se você receber um ponteiro de interface [**IDispatch,**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) use-o com **CHILDID \_ SELF** para acessar propriedades e métodos de interface [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)<br/> Se a chamada para [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) falhar, você terá um elemento simples. Use o ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original (aquele usado na chamada para o método ou função mencionado acima) com a ID filho **\_ VT I4** retornada pela chamada.<br/> |



 

Antes de usar um [**parâmetro VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) você deve inicializá-lo chamando a função [**VARIANTInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM). Quando terminar com a estrutura, chame [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) para liberar a memória reservada para essa **VARIANT.**

## <a name="special-cases"></a>Casos especiais

Há exceções às diretrizes na tabela acima, como quando uma ID filho é retornada pelo método [**IAccessible::accHitTest.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) Os servidores deverão retornar uma interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) se o filho for um objeto acessível. Se uma ID filho for retornada por **IAccessible::accHitTest**, o filho será um elemento simples.

Além disso, há casos especiais para [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate). Para obter mais informações, **consulte IAccessible::accNavigate** e [Navegação Espacial e Lógica.](spatial-and-logical-navigation.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[IDispatch Interface](idispatch-interface.md)
</dt> <dt>

[Estrutura VARIANT](variant-structure.md)
</dt> </dl>

 

