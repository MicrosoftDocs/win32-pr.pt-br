---
description: A Propriedade ColumnInfo do objeto View retorna um objeto Record contendo as informações solicitadas sobre cada coluna no conjunto de resultados.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: Propriedade View. ColumnInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.ColumnInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 38c016b15108446cc04114adc06ad12686d9932c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752236"
---
# <a name="viewcolumninfo-property"></a>Propriedade View. ColumnInfo

A propriedade **ColumnInfo** do objeto [**View**](view-object.md) retorna um objeto [**Record**](record-object.md) contendo as informações solicitadas sobre cada coluna no conjunto de resultados. Os nomes de coluna ou as definições de coluna podem ser solicitadas. As constantes fornecidas na lista de seleção não têm nomes.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Valor da propriedade

Informações obrigatórias necessárias para cada coluna.



| Nome do parâmetro                                                                                                                                                                                                                                                          | Significado                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | Retorna os nomes de todas as colunas não constantes no conjunto de resultados.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | Retorna os tipos de todas as colunas não constantes no conjunto de resultados.<br/> |



 

## <a name="remarks"></a>Comentários

As descrições de coluna retornadas pela propriedade **ColumnInfo** estão no formato descrito em [formato de definição de coluna](column-definition-format.md). Cada coluna é descrita por uma cadeia de caracteres no campo registro correspondente. A cadeia de caracteres de definição consiste em uma única letra que representa o tipo de dados seguido pela largura da coluna (em caracteres quando aplicável, ou outros bytes). Uma largura de zero designa uma largura não associada (fluxos e campos de texto longos). Uma letra maiúscula indica que valores nulos são permitidos na coluna.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




