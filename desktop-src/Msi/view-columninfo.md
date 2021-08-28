---
description: A propriedade ColumnInfo do objeto View retorna um objeto Record que contém as informações solicitadas sobre cada coluna no conjunto de resultados.
ms.assetid: 8cfa504c-a6f1-443e-9b3a-b230c4c39b64
title: Propriedade View.ColumnInfo
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
ms.openlocfilehash: 08996c3e77212032eac8f65621c7f8ca9ee8489683295c63fb30092995ad41d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012694"
---
# <a name="viewcolumninfo-property"></a>Propriedade View.ColumnInfo

A **propriedade ColumnInfo** do objeto [**View**](view-object.md) retorna um [**objeto Record**](record-object.md) que contém as informações solicitadas sobre cada coluna no conjunto de resultados. Os nomes de coluna ou as definições de coluna podem ser solicitados. As constantes fornecidas na lista Selecionar não têm nomes.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = View.ColumnInfo
```



## <a name="property-value"></a>Valor da propriedade

Informações necessárias para cada coluna.



| Nome do parâmetro                                                                                                                                                                                                                                                          | Significado                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="msiColumnInfoNames"></span><span id="msicolumninfonames"></span><span id="MSICOLUMNINFONAMES"></span><dl> <dt>**msiColumnInfoNames**</dt> <dt>0</dt> </dl> | Retorna os nomes de todas as colunas nãoconstantes no conjunto de resultados.<br/> |
| <span id="msiColumnInfoTypes"></span><span id="msicolumninfotypes"></span><span id="MSICOLUMNINFOTYPES"></span><dl> <dt>**msiColumnInfoTypes**</dt> <dt>1</dt> </dl> | Retorna os tipos de todas as colunas nãoconstantes no conjunto de resultados.<br/> |



 

## <a name="remarks"></a>Comentários

As descrições de coluna retornadas pela **propriedade ColumnInfo** estão no formato descrito em [Formato de Definição de Coluna](column-definition-format.md). Cada coluna é descrita por uma cadeia de caracteres no campo de registro correspondente. A cadeia de caracteres de definição consiste em uma única letra que representa o tipo de dados seguido pela largura da coluna (em caracteres quando aplicável ou bytes). Uma largura de zero designa uma largura não unidas (fluxos e campos de texto longos). Uma letra maiúscula indica que valores nulos são permitidos na coluna.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView é definido como \_ 000C109C-0000-0000-C000-00000000046<br/>                                                                                                                                                                                |



 

 




