---
description: Usado por aplicativos para exibir uma caixa de diálogo de dispositivo para o usuário.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Função DeviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790552"
---
# <a name="devicedialog-function"></a>Função DeviceDialog

Usado por aplicativos para exibir uma caixa de diálogo de dispositivo para o usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDeviceDialogData* \[ no\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA**

O [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) a ser usado para criar a caixa de diálogo do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




