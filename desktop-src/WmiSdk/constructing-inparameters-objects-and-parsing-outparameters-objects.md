---
description: Normalmente, o acesso direto é adequado para chamar um método de provedor WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Construindo objetos de inparâmetros e analisando objetos de Parameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922202"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a>Construindo objetos de inparâmetros e analisando objetos de Parameters

Normalmente, o acesso direto é adequado para chamar um [*método de provedor*](gloss-p.md)WMI. Acesso direto significa executar um método usando a sintaxe *Object. Method* . No entanto, em alguns casos, o acesso direto não pode ser usado. Além disso, chamar um método de provedor de forma assíncrona de um script requer um tipo de chamada [**ExecMethodAsync**](swbemobject-execmethodasync-.md) .

> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

A ordem dos parâmetros de entrada e saída do método é definida no esquema formato MOF (MOF) para o método. O WMI não impede que a ordem do parâmetro seja alterada quando a classe é recompilada pelo [Mofcomp](mofcomp.md). Usando um objeto de [**inparâmetros**](swbemmethod-inparameters.md) , você pode evitar problemas resultantes do esquema alterado porque os parâmetros de entrada são identificados por nome. O parâmetro correto pode ser visto examinando o qualificador de **ID** de cada parâmetro de entrada. O primeiro parâmetro tem um valor de **ID** igual a 0 (zero).

[**Os métodos SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) fornecem uma maneira alternativa de executar um método de provedor em casos em que não é possível executar um método diretamente. Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

Para obter mais informações sobre parâmetros, consulte [construindo objetos de inparâmetros](constructing-inparameters-objects.md) e [analisando objetos de Parameters](parsing-outparameters-objects.md).

 

 



