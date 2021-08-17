---
title: Visual Basic AccValue de notas de método
description: O arquivo de linguagem de descrição de objeto (ODL), OleAcc. ODL, contém informações que diferem da implementação de C/C++. O arquivo OleAcc. odl contém a seguinte definição para a versão que define a propriedade da função.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f5a79740e71984b4d9beaba9faad23142b2c9afc78a7378e9b11be4dc521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744776"
---
# <a name="visual-basic-method-notes-accvalue"></a>Visual Basic Observações do método: accValue

O arquivo de linguagem de descrição de objeto (ODL), OleAcc. ODL, contém informações que diferem da implementação de C/C++. O arquivo OleAcc. odl contém a seguinte definição para a versão que define a propriedade da função.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Embora o parâmetro *varChild* esteja listado como opcional no arquivo ODL e no Pesquisador de objetos, você deve incluí-lo ao chamar a versão de configuração de Propriedade do [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




