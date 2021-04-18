---
description: A Propriedade Property do objeto Session é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador, conforme mantida pelo objeto Session.
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Propriedade Session. Property
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
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792483"
---
# <a name="sessionproperty-property"></a>Propriedade Session. Property

A propriedade **Property** do objeto [**Session**](session-object.md) é uma propriedade de leitura/gravação que representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador, conforme mantida pelo objeto de **sessão** na tabela de propriedades na memória, ou, se for prefixada com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual. Os valores de cadeia de caracteres ou inteiros podem ser fornecidos. Uma propriedade ou variável de ambiente não existente é equivalente ao valor que está sendo nulo.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>Valor da propriedade

O nome de uma propriedade que diferencia maiúsculas de minúsculas ou um nome que não diferencia maiúsculas de minúsculas de uma variável de ambiente prefixado por um sinal de porcentagem (%).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




