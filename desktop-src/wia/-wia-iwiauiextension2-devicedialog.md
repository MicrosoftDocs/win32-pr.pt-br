---
description: IWiaUIExtension2::D método eviceDialog – fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: 'IWiaUIExtension2: método eviceDialog de:D (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 94e717184c936ae85ba1cf345a13b44f9bbdce4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116644"
---
# <a name="iwiauiextension2devicedialog-method"></a>IWiaUIExtension2: método eviceDialog de:D

Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDeviceDialogData* \[ no\]
</dt> <dd>

Tipo: **PDEVICEDIALOGDATA2 \***

Aponta para uma estrutura [**DEVICEDIALOGDATA2**](-wia-devicedialogdata2.md) que contém todos os dados necessários para implementar a caixa de diálogo do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se o método for bem sucedido, ele retornará S \_ OK. Se o usuário cancelar a caixa de diálogo, o método retornará S \_ false. Se o método falhar, ele retornará um código de erro apropriado. A tabela a seguir mostra alguns dos possíveis códigos de status de retorno.



| Código do erro    | Descrição                              |
|---------------|------------------------------------------|
| E \_ INVALIDARG | O parâmetro pDeviceDialogData é **nulo**. |
| E \_ NOTIMPL    | O método não está implementado.           |



 

## <a name="remarks"></a>Comentários

Se você implementar a interface [**IWiaUIExtension2**](-wia-iwiauiextension2.md) e não quiser substituir a interface do usuário do sistema, esse método ainda deverá ser implementado, mas não deverá fazer nada mais do que Return E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 




