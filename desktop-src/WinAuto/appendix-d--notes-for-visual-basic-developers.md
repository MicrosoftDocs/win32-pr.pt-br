---
title: Apêndice D notas para desenvolvedores de Visual Basic
description: Esta seção fornece informações sobre o Microsoft Acessibilidade Ativa para desenvolvedores do Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916216"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Apêndice D: notas para desenvolvedores de Visual Basic

Esta seção fornece informações sobre o Microsoft Acessibilidade Ativa para desenvolvedores do Microsoft Visual Basic.

Os aplicativos escritos em Visual Basic são clientes do Microsoft Acessibilidade Ativa. Eles não fornecem informações sobre seus elementos personalizados da interface do usuário porque não implementam o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou qualquer outra interface COM (Component Object Model).

Esta documentação usa os nomes de C/C++ para as propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ; no entanto, os nomes de Visual Basic são semelhantes. Por exemplo, a propriedade [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) seria chamada de **accName** em um aplicativo Visual Basic.

## <a name="in-this-section"></a>Nesta seção

-   [Visual Basic observações do método: accName](visual-basic-method-notes--accname.md)
-   [Visual Basic observações do método: accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic programas de exemplo](visual-basic-sample-programs.md)

 

 




