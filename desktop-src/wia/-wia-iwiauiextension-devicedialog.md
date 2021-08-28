---
description: Método IWiaUIExtension::D eviceDialog – fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: Método IWiaUIExtension::D eviceDialog (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: a06ac5428743c31bae22c6d106ee927791739295754b15ac9764045c3aeeffab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813866"
---
# <a name="iwiauiextensiondevicedialog-method"></a>Método IWiaUIExtension::D eviceDialog

Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDeviceDialogData* \[ Em\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA \***

Aponta para uma [**estrutura DEVICEDIALOGDATA**](-wia-devicedialogdata.md) que contém todos os dados necessários para implementar a caixa de diálogo do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se o método for bem-sucedido, ele retornará S \_ OK. Se o usuário cancelar a caixa de diálogo, o método retornará S \_ FALSE. Se o método não for implementado, ele retornará E \_ NOTIMPL. Se o método falhar, ele retornará um código de erro COM padrão.

## <a name="remarks"></a>Comentários

Se você implementar a interface [**IWiaUIExtension**](-wia-iwiauiextension.md) e não quiser substituir a interface do usuário do sistema, esse método ainda deverá ser implementado, mas não deverá fazer nada além de retornar E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 




