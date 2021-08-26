---
title: Usar OBJID \_ NATIVEOM para expor uma interface nativa para uma janela
description: Essa técnica permite que os clientes obtenham um objeto personalizado para uma janela. Os servidores podem usar isso para expor um ponteiro para um objeto de documento personalizado para uma janela.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed99db4641235ceee57688865710c19a41f0a517d70d4601d138150cb88dd470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098086"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a>Usar OBJID \_ NATIVEOM para expor uma interface nativa para uma janela

Essa técnica permite que os clientes obtenham um objeto personalizado para uma janela. Os servidores podem usar isso para expor um ponteiro para um objeto de documento personalizado para uma janela.

**Para expor uma interface de modelo de objeto nativo para uma janela (servidores)**

1.  Manipule a mensagem do [**WM \_ GetObject**](wm-getobject.md) no procedimento de janela. Quando o valor de *lParam* é [**OBJID \_ NATIVEOM**](object-identifiers.md), retorna um ponteiro de interface para o objeto personalizado usando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).
2.  Libere o ponteiro de interface depois de chamar [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), se apropriado. Para obter mais informações, consulte **LresultFromObject**.

Os clientes podem obter um ponteiro para esse objeto personalizado.

**Para obter um ponteiro para um objeto personalizado para uma janela (clientes)**

-   Chame [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e passe [**OBJID \_ NATIVEOM**](object-identifiers.md) como o segundo parâmetro.

Observe os seguintes problemas para essa técnica:

-   Essa técnica é semelhante a retornar um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , exceto para a ID de objeto usada e o fato de que [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) retorna um objeto personalizado em vez de **IAccessible**.
-   Os desenvolvedores de servidor podem precisar publicar informações que permitam aos clientes identificar exclusivamente o **HWND** para que possam encontrá-lo antes de chamar [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) em seu identificador de janela.
-   Não implemente a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no objeto personalizado que é retornado. Se você fizer isso, o OLEACC tratará como uma **IAccessible** padrão e poderá impedir que as interfaces personalizadas sejam usadas.
-   Para ser usado em vários processos, as interfaces no objeto retornado podem precisar ser registradas com Component Object Model (COM).

essa técnica é compatível com vários componentes Microsoft Office. Para obter mais informações, consulte [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

 

 




