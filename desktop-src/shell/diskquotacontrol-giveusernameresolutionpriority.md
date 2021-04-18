---
description: Coloca o objeto de usuário especificado próximo na linha para resolução de nomes.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Método DiskQuotaControl. GiveUserNameResolutionPriority (Dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501415"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a>Método DiskQuotaControl. GiveUserNameResolutionPriority

Coloca o objeto de usuário especificado próximo na linha para resolução de nomes.

## <a name="syntax"></a>Sintaxe


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*oUser* 
</dt> <dd>

Tipo: **objeto**

Uma expressão de objeto que é avaliada como o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) do usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a resolução assíncrona de nomes estiver habilitada, os objetos de usuário serão colocados em uma fila. Por padrão, eles são atendidos na ordem em que são colocados na fila. O método **GiveUserNameResolutionPriority** move um objeto para a frente da fila para que ele seja o próximo da linha a ser atendida.

Use a propriedade [**UserNameResolution**](diskquotacontrol-usernameresolution.md) para habilitar a resolução de nome assíncrona.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




