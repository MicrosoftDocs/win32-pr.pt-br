---
description: A propriedade Property do objeto Session é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade do instalador nomeado, conforme mantido pelo objeto Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Propriedade Session.Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7f47efd603f10378e6cf5b09144d57776a42cd515f3bd6194174d94bc2583514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628826"
---
# <a name="sessionproperty-property"></a>Propriedade Session.Property

A  propriedade Property [](session-object.md) do objeto Session é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade do instalador nomeado, conforme mantido pelo objeto **Session** na tabela Propriedade na memória ou, se for prefixado com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual. Valores de cadeia de caracteres ou inteiros podem ser fornecidos. Uma propriedade ou variável de ambiente inexistente é equivalente ao seu valor ser Null.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Valor da propriedade

Nome necessário que não faça maiúsculas de minúsculas de uma propriedade ou um nome que não não faça maiúsculas de minúsculas de uma variável de ambiente prefixada por um sinal de porcentagem (%).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession é definido como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




