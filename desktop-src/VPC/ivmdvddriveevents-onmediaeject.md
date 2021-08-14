---
title: Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Recebe a notificação de que a mídia foi ejetada da unidade. | Método IVMDVDDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- OnMediaEject do método virtual PC
- Método OnMediaEject Virtual PC, interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface virtual PC, método OnMediaEject
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2fbf9ffe589597e1baab7c0b503cf94384cfa540749cfe49e083286f743370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753747"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a>Método IVMDVDDriveEvents:: OnMediaEject

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe a notificação de que a mídia foi ejetada da unidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mediaPath* \[ no\]
</dt> <dd>

A letra da unidade do host, ou caminho, para a imagem ISO.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado quando a mídia (uma imagem ISO ou um disco em uma unidade de host) é ejetada. O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento Onejeção vmDVDDriveEvent originário de [**IVMDVDDrive**](ivmdvddrive.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents é definido como c2a7d8e9-E76C-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

