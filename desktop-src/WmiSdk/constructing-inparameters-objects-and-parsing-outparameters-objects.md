---
description: Normalmente, o acesso direto é adequado para chamar um método de provedor WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Construindo objetos InParameters e análise de objetos OutParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edda8255fa40baa44792e0dc2c719431cdf62c0c5a75bb9aa90221dc84e48f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819458"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a>Construindo objetos InParameters e análise de objetos OutParameters

Normalmente, o acesso direto é adequado para chamar um método de provedor [*WMI*](gloss-p.md). Acesso direto significa executar um método usando a *sintaxe object.method.* No entanto, em alguns casos, o acesso direto não pode ser usado. Além disso, chamar um método de provedor de forma assíncrona de um script requer um tipo de chamada [**ExecMethodAsync.**](swbemobject-execmethodasync-.md)

> [!Note]  
> Como o retorno de chamada para o sink pode não ser retornado no mesmo nível de autenticação que o cliente exige, é recomendável que você use a comunicação síncrona em vez de assíncrona. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

 

A ordem dos parâmetros de entrada e saída do método é definida no esquema Managed Object Format (MOF) para o método . O WMI não impede que a ordem do parâmetro seja alterada quando a classe é recompilada por [mofcomp.](mofcomp.md) Usando um [**objeto InParameters,**](swbemmethod-inparameters.md) você pode evitar problemas resultantes de um esquema alterado porque os parâmetros de entrada são identificados pelo nome. O parâmetro correto pode ser visto examinando o qualificador **de ID** de cada parâmetro de entrada. O primeiro parâmetro tem um **valor de ID** de 0 (zero).

Os [**métodos SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md),SWbemObject.Exe [**cMethodAsync, \_**](swbemobject-execmethodasync-.md)SWbemServices.Exe [**cMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) fornecem uma maneira alternativa de executar um método de provedor em casos em que não é possível executar um método diretamente. Para obter mais informações, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

Para obter mais informações sobre parâmetros, consulte [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).

 

 



