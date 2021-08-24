---
title: Método IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
description: Recebe a notificação de que a mídia foi ejetada da unidade. | Método IVMFloppyDriveEvents OnMediaEject (VPCCOMInterfaces. h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- OnMediaEject do método virtual PC
- Método OnMediaEject Virtual PC, interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface virtual PC, método OnMediaEject
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e624dcbf028caf58a2f50109789e5f89cd34d1d70c4679333b8b742c3b071ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653596"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a>Método IVMFloppyDriveEvents:: OnMediaEject

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

A letra da unidade do host, ou caminho, para a imagem do disquete.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado quando a mídia (uma imagem de disquete ou um disquete em uma unidade de host) é ejetada. O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmFloppyDriveEvent OnMediaEject originado do [**IVMFloppyDrive**](ivmfloppydrive.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents é definido como a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

