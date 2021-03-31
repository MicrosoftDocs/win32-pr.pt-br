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
# <a name="visual-basic-method-notes-accvalue"></a><span data-ttu-id="5c519-104">Visual Basic observações do método: accValue</span><span class="sxs-lookup"><span data-stu-id="5c519-104">Visual Basic Method Notes: accValue</span></span>

<span data-ttu-id="5c519-105">O arquivo de linguagem de descrição de objeto (ODL), OleAcc. ODL, contém informações que diferem da implementação de C/C++.</span><span class="sxs-lookup"><span data-stu-id="5c519-105">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="5c519-106">O arquivo OleAcc. odl contém a seguinte definição para a versão que define a propriedade da função.</span><span class="sxs-lookup"><span data-stu-id="5c519-106">The file Oleacc.odl contains the following definition for the version that sets the property of the function.</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



<span data-ttu-id="5c519-107">Embora o parâmetro *varChild* esteja listado como opcional no arquivo ODL e no Pesquisador de objetos, você deve incluí-lo ao chamar a versão de configuração de Propriedade do [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span><span class="sxs-lookup"><span data-stu-id="5c519-107">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span></span>

 

 




