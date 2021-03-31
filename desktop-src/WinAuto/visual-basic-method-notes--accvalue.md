---
title: Visual Basic de observações do método accValue
description: O arquivo de linguagem de descrição de objeto (ODL), OleAcc. ODL, contém informações que diferem da implementação de C/C++. O arquivo OleAcc. odl contém a seguinte definição para a versão que define a propriedade da função.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce93bc5d4ff2a2e01da55e30630fda42c573b7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005367"
---
# <a name="visual-basic-method-notes-accvalue"></a>Visual Basic observações do método: accValue

O arquivo de linguagem de descrição de objeto (ODL), OleAcc. ODL, contém informações que diferem da implementação de C/C++. O arquivo OleAcc. odl contém a seguinte definição para a versão que define a propriedade da função.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Embora o parâmetro *varChild* esteja listado como opcional no arquivo ODL e no Pesquisador de objetos, você deve incluí-lo ao chamar a versão de configuração de Propriedade do [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




