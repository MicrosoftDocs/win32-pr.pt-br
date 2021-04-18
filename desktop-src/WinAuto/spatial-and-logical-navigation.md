---
title: Navegação espacial e lógica
description: Os clientes recuperam informações sobre um objeto que é espacial ou logicamente próximo a outro objeto dentro do mesmo contêiner chamando IAccessible accNavigate e especificando uma das constantes de navegação.
ms.assetid: a1ebb50e-76cf-472d-bb0f-3f5bf5ed30d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e49772a267e49d723a04005dcbc8a369510b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105771377"
---
# <a name="spatial-and-logical-navigation"></a>Navegação espacial e lógica

Os clientes recuperam informações sobre um objeto que é espacial ou logicamente próximo a outro objeto dentro do mesmo contêiner chamando [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) e especificando uma das [constantes de navegação](navigation-constants.md).

Com clientes de *navegação espacial* , navegue até um objeto com base em sua localização na tela. Os clientes navegam para cima, para baixo, para a esquerda ou para a direita do objeto atual para obter informações sobre outro objeto dentro do mesmo contêiner.

Com os clientes de *navegação lógicos* , navegue até o objeto que precede logicamente ou segue outro objeto, conforme determinado pelo servidor. Os clientes navegam para todos os filhos de um objeto de duas maneiras:

-   Inicie a navegação com [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) e, em seguida, chame repetidamente o método com [**NAVDIR \_ Next**](navigation-constants.md).
-   Inicie a navegação com [**NAVDIR \_ LASTCHILD**](navigation-constants.md) e chame repetidamente o método com [**NAVDIR \_ anterior**](navigation-constants.md).

Independentemente da direção, a navegação visita cada filho visível que pertence ao objeto pai. Os filhos invisíveis podem ser ignorados com navegação lógica. Além disso, cada filho é visitado apenas uma vez, e a navegação não faz um loop. Ou seja, o método falhará se um cliente tentar navegar antes do primeiro objeto ou após o último objeto.

A navegação espacial e lógica estão relacionadas. Por exemplo, em uma barra de ferramentas horizontal, chamar o método com o [**\_ direito NAVDIR**](navigation-constants.md) deve produzir os mesmos resultados que chamar o método com [**NAVDIR \_ Next**](navigation-constants.md).

O objeto inicial da navegação é o objeto **próprio ou um dos filhos do objeto, exceto quando** [**NAVDIR \_ FIRSTCHILD**](navigation-constants.md) ou [**NAVDIR \_ LASTCHILD**](navigation-constants.md) é especificado; nesse caso, a navegação deve iniciar a partir do próprio objeto.

Se um cliente navegar de um objeto acessível para um elemento de interface do usuário irmão, ou se o membro **lVal** de *varStart* for **filhaid \_** e o sinalizador especificado em *NavDir* for qualquer sinalizador de navegação, exceto [**navdir \_ FIRSTCHILD**](navigation-constants.md) ou [**navdir \_ LASTCHILD**](navigation-constants.md), o resultado em *pvarEnd* será uma ID filho ou uma interface [**IDispatch**](idispatch-interface.md) . Se *pvarEnd* contiver uma ID filho, os clientes deverão primeiro obter um ponteiro para a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do pai a fim de navegar por esse elemento da interface do usuário ou para obter mais informações sobre ele. Para obter o objeto pai, os clientes chamam a propriedade [**IAccessible:: get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) do objeto irmão ou o objeto inicial da navegação.

Observe que os clientes devem ter informações sobre todos os objetos flutuantes chamando a função [**EnumChildWindows**](/windows/desktop/api/winuser/nf-winuser-enumchildwindows) . Como um objeto flutuante não é recortado para seu pai, os clientes não têm informações sobre a relação hierárquica entre dois objetos próximos um do outro na tela.

O gráfico a seguir é um exemplo de um objeto flutuante que não é recortado em seu pai.

![captura de tela da janela aberta flutuante acima de uma janela maior do Microsoft Developer Studio](images/floatob.gif)

## <a name="establishing-the-order-in-logical-navigation"></a>Estabelecendo a ordem na navegação lógica

Na navegação lógica, os desenvolvedores que criam os objetos estabelecem as relações entre eles. A navegação lógica é mais subjetiva do que a navegação espacial. Além disso, a ordem na navegação lógica não é a mesma que a ordem usada com as IDs filho.

Para objetos que têm locais de tela, os desenvolvedores de servidor devem estabelecer a ordem de navegação da maneira que a maioria dos usuários consideraria lógica. Em países/regiões de língua inglesa, por exemplo, isso significa uma ordenação da esquerda para a direita, de cima para baixo.

A ordem de navegação lógica deve ser uma ordem de navegação de teclado paralela. Por exemplo, uma caixa de diálogo contém botões **OK** e **Cancelar** push e alguns controles de edição. Um cliente que chama [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para navegar até o objeto seguinte ou anterior nessa caixa de diálogo se move na mesma ordem que um usuário pressionando TAB ou Shift + Tab para mover o foco entre os itens.

Para objetos que não têm locais de tela definidos, a ordem lógica é decidida por desenvolvedores de servidor e os desenvolvedores de cliente não devem fazer suposições sobre ele. Por exemplo, é aceitável que objetos não visíveis, como objetos que estão temporariamente ocultos, sejam intercalados com objetos visíveis.

 

 