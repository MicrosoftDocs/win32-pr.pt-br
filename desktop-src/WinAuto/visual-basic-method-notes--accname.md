---
title: Visual Basic de observações do método accName
description: O arquivo de linguagem de descrição de objeto (ODL), OleAcc. ODL, contém informações que diferem da implementação de C/C++.
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c404c093fc3b92b4d653b0b1258c62918af8e25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822684"
---
# <a name="visual-basic-method-notes-accname"></a>Visual Basic observações do método: accName

O arquivo de linguagem de descrição de objeto (ODL), OleAcc. ODL, contém informações que diferem da implementação de C/C++. O arquivo OleAcc. odl contém a seguinte definição para a versão que define a propriedade da função:


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



Embora o parâmetro *varChild* esteja listado como opcional no arquivo ODL e no Pesquisador de objetos, você deve incluí-lo ao chamar a versão de configuração de Propriedade do [**accName**](https://www.bing.com/search?q=**accName**).

 

 




