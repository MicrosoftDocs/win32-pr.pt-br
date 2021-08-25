---
description: A propriedade DataSize do objeto Record é uma propriedade somente leitura que retorna o tamanho dos dados para o campo designado.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Propriedade Record.DataSize
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
ms.openlocfilehash: 067fc09e65d644413e75ccd8a9c0173e30df8060dff0f772ae5d12705ab610aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912956"
---
# <a name="recorddatasize-property"></a>Propriedade Record.DataSize

A **propriedade DataSize** do [**objeto Record**](record-object.md) é uma propriedade somente leitura que retorna o tamanho dos dados para o campo designado. Se os dados são um fluxo, o comprimento do fluxo em bytes é retornado. Se os dados são uma cadeia de caracteres, o comprimento da cadeia de caracteres sem Null será retornado. Se os dados são um inteiro, o valor 4 é retornado (indicando o tamanho do inteiro). Se os dados são Nulos, 0 é retornado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a>Valor da propriedade

Número de campo necessário do valor dentro do registro, com base em 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord é definido como 000C1093-0000-0000-C000-00000000046<br/>                                                                                                                                                                              |



 

 




