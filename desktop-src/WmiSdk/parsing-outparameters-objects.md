---
description: Um objeto SWbemMethod. Parameters é criado e fornecido com dados pelo método de provedor em execução.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Analisando objetos de Parameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297428"
---
# <a name="parsing-outparameters-objects"></a>Analisando objetos de Parameters

Um objeto [**SWbemMethod. Parameters**](swbemmethod-outparameters.md) é criado e fornecido com dados pelo método de provedor em execução. As propriedades do objeto **Parameters** são específicas para o método chamado. Por exemplo, no script abaixo, o *SD* (contido em *OutParam*) é o parâmetro de saída definido para o método **\_ \_ SystemSecurity. gets** . A propriedade **ReturnValue** é uma propriedade genérica disponível para todos os objetos de **Parameters** que contêm o resultado da operação.

O exemplo de código a seguir ilustra a [**obtenção de parâmetros**](--systemsecurity-getsd.md) de saída da execução do método obtido na classe [**\_ \_ SystemSecurity**](--systemsecurity.md) para o sistema local.


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



Para obter mais informações, consulte [**SWbemMethod. Parameters**](swbemmethod-inparameters.md).

 

 



