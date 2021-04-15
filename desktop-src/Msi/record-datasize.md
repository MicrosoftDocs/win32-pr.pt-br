---
description: A propriedade DataSize do objeto Record é uma propriedade somente leitura que retorna o tamanho dos dados para o campo designado.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Propriedade Record. DataSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747324"
---
# <a name="recorddatasize-property"></a>Propriedade Record. DataSize

A propriedade **DataSize** do objeto [**Record**](record-object.md) é uma propriedade somente leitura que retorna o tamanho dos dados para o campo designado. Se os dados forem um fluxo, o tamanho do fluxo em bytes será retornado. Se os dados forem uma cadeia de caracteres, o comprimento da cadeia de caracteres sem NULL será retornado. Se os dados forem um inteiro, o valor 4 será retornado (indicando o tamanho do inteiro). Se os dados forem nulos, 0 será retornado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Valor da propriedade

Campo obrigatório número do valor dentro do registro, baseado em 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




