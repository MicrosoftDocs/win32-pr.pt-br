---
title: Apêndice D Notes for Visual Basic Developers
description: Esta seção fornece informações sobre o Microsoft Active Accessibility para desenvolvedores Visual Basic Microsoft.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a857aeb8e04a0648d991e26913f9a9cf5c35328c62ed3f1ac3903a267e5a4e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122416"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Apêndice D: Observações para Visual Basic desenvolvedores

Esta seção fornece informações sobre o Microsoft Active Accessibility para desenvolvedores Visual Basic Microsoft.

Os aplicativos escritos Visual Basic são Microsoft Active Accessibility clientes. Eles não fornecem informações sobre seus elementos de interface do usuário personalizados porque não implementam [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou qualquer outra interface com Component Object Model (COM).

Esta documentação usa os nomes C/C++ para as [**propriedades IAccessible;**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no entanto, os Visual Basic nomes são semelhantes. Por exemplo, a [**propriedade IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) seria chamada **accName** em um Visual Basic aplicativo.

## <a name="in-this-section"></a>Nesta seção

-   [Visual Basic Notas de método: accName](visual-basic-method-notes--accname.md)
-   [Visual Basic Notas de método: accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic Programas de exemplo](visual-basic-sample-programs.md)

 

 




