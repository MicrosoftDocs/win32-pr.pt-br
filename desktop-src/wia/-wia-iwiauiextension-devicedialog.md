---
description: IWiaUIExtension::D método eviceDialog – fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: 'IWiaUIExtension: método eviceDialog de:D (Wiadevd. h)'
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
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116704"
---
# <a name="iwiauiextensiondevicedialog-method"></a>IWiaUIExtension: método eviceDialog de:D

Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDeviceDialogData* \[ no\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA \***

Aponta para uma estrutura [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) que contém todos os dados necessários para implementar a caixa de diálogo do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se o método for bem sucedido, ele retornará S \_ OK. Se o usuário cancelar a caixa de diálogo, o método retornará S \_ false. Se o método não for implementado, ele retornará E \_ NOTIMPL. Se o método falhar, ele retornará um código de erro COM padrão.

## <a name="remarks"></a>Comentários

Se você implementar a interface [**IWiaUIExtension**](-wia-iwiauiextension.md) e não quiser substituir a interface do usuário do sistema, esse método ainda deverá ser implementado, mas não deverá fazer nada mais do que Return E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




