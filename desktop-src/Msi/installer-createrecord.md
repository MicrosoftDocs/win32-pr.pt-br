---
description: O método CreateRecord do objeto instalador retorna um novo objeto de registro com o número de campos solicitado.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Método Installer. CreateRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752038"
---
# <a name="installercreaterecord-method"></a>Método Installer. CreateRecord

O método **CreateRecord** do objeto [**instalador**](installer-object.md) retorna um novo objeto de [**registro**](record-object.md) com o número de campos solicitado.

## <a name="syntax"></a>Sintaxe


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*contagem* 
</dt> <dd>

Número necessário de campos, que pode ser 0. O número máximo de campos em um registro é limitado a 65535.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O campo 0, não um dos campos em *contagem*, normalmente é usado para itens orientados a registros, como cadeias de caracteres de formato ou códigos op de execução.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




