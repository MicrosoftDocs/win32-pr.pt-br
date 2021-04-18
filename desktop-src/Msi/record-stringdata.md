---
description: A propriedade StringData do objeto Record é uma propriedade de leitura/gravação que transfere dados de cadeia de caracteres para dentro ou para fora de um campo especificado no registro. Se um inteiro ou um objeto tiver sido armazenado, seu valor de cadeia de caracteres será retornado.
ms.assetid: ffa163eb-41b3-47ae-b01d-39a3890990a3
title: Propriedade Record. StringData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.StringData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 21f72c35795696875aa55f2d5d791564c6f1fee5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756722"
---
# <a name="recordstringdata-property"></a>Propriedade Record. StringData

A propriedade **StringData** do objeto [**Record**](record-object.md) é uma propriedade de leitura/gravação que transfere dados de cadeia de caracteres para dentro ou para fora de um campo especificado no registro. Se um inteiro ou um objeto tiver sido armazenado, seu valor de cadeia de caracteres será retornado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.StringData
Record.StringData = propVal 
```



## <a name="property-value"></a>Valor da propriedade

Campo obrigatório número do valor dentro do registro, baseado em 1.

## <a name="remarks"></a>Comentários

O valor retornado de um campo inexistente é uma cadeia de caracteres vazia. Para definir um campo de cadeia de caracteres de registro como nulo, use uma variante vazia ou uma cadeia de caracteres vazia. A tentativa de armazenar um valor em um campo inexistente causa um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




