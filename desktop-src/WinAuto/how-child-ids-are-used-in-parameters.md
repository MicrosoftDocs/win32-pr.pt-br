---
title: Como as IDs filho são usadas nos parâmetros
description: Este tópico descreve os parâmetros de entrada, os parâmetros de saída e os casos especiais para interpretar IDs filho retornadas de métodos IAccessible.
ms.assetid: 051ec5ba-540c-4ae1-b917-4c229557ca2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03026e6abf769efab95cc513231fad3af64511f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366261"
---
# <a name="how-child-ids-are-used-in-parameters"></a>Como as IDs filho são usadas nos parâmetros

Este tópico descreve os parâmetros de entrada, os parâmetros de saída e os casos especiais para interpretar IDs filho retornadas de métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

## <a name="input-parameters"></a>Parâmetros de Entrada

Muitas das funções do Microsoft Acessibilidade Ativa e a maioria das propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) usam uma estrutura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) como um parâmetro de entrada. Para a maioria das propriedades **IAccessible** , esse parâmetro permite que os desenvolvedores de clientes especifiquem se desejam informações sobre o próprio objeto ou sobre um dos elementos simples do objeto.

O Microsoft Acessibilidade Ativa fornece a constante **filhaid \_ própria** para indicar que as informações são necessárias sobre o próprio objeto. Para obter informações sobre um elemento simples, os desenvolvedores de cliente especificam sua ID filho no parâmetro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .

Ao inicializar um parâmetro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , certifique-se de **especificar \_ VT i4** no membro **VT** , além de especificar o valor da ID filho (ou **childID \_ próprio**) no membro **lVal** .

Por exemplo, para obter o nome de um objeto e não um dos elementos filho do objeto, inicialize a [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) para o primeiro parâmetro de [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) ( **filhaid \_ própria** no membro **lVal** e **VT \_ i4** no membro **VT** ) e, em seguida, chame **IAccessible:: get \_ accName**.

## <a name="output-parameters"></a>Parâmetros de saída

Várias funções e métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) têm um [](/windows/win32/api/oaidl/ns-oaidl-variant) \* parâmetro de saída variante que contém uma ID filho ou um ponteiro de interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) para um objeto filho. Há diferentes etapas que um cliente deve executar, dependendo se receberá uma ID de filho **VT \_ i4** (elemento simples) ou um ponteiro de interface **IDispatch** com **childID \_ próprio** (objeto completo). Seguir essas etapas fornecerá um ponteiro de interface **IAccessible** e uma ID filho que, juntos, permitem que os clientes usem os métodos e as propriedades do **IAccessible** . Essas etapas se aplicam aos métodos [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest), [**Get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)e [**Get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) . Eles também se aplicam às funções de cliente [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)e [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) .

A tabela a seguir lista o possível resultado retornado e as etapas de pós-processamento necessárias para que os clientes tenham um ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e uma ID filho.



| Resultado retornado                                      | Pós-processamento para o valor de retorno                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ponteiro de interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) | Este é um objeto completo. Chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para acessar o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Use o ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) com **childID \_ próprio** para acessar métodos e propriedades do **IAccessible** .<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| \_ID filho de VT i4                                      | Chame [**IAccessible:: get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) usando a ID filho para ver se você tem um ponteiro de interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) . Se você receber um ponteiro de interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) , use-o com o **childID \_ próprio** para acessar métodos e propriedades da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .<br/> Se a chamada para [**Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) falhar, você terá um elemento simples. Use o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original (aquele que você usou em sua chamada para o método ou função mencionado acima) com a ID filho **VT \_ i4** que a chamada retornou.<br/> |



 

Antes de usar um parâmetro [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , você deve inicializá-lo chamando a função com ( [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model). Quando terminar com a estrutura, chame [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear) para liberar a memória reservada para essa **variante**.

## <a name="special-cases"></a>Casos especiais

Há exceções às diretrizes na tabela acima, como quando uma ID filho é retornada pelo método [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) . Os servidores devem retornar uma interface [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) se o filho for um objeto acessível. Se uma ID filho for retornada por **IAccessible:: accHitTest**, o filho será um elemento simples.

Além disso, há casos especiais para [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate). Para obter mais informações, consulte **IAccessible:: accNavigate** e a [navegação lógica e espacial](spatial-and-logical-navigation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Interface IDispatch](idispatch-interface.md)
</dt> <dt>

[Estrutura de variante](variant-structure.md)
</dt> </dl>

 

