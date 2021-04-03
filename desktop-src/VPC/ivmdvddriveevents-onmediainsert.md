---
title: Método IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
description: Recebe a notificação de que a mídia foi inserida na unidade. | Método IVMDVDDriveEvents OnMediaInsert (VPCCOMInterfaces. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- OnMediaInsert do método virtual PC
- Método OnMediaInsert Virtual PC, interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface virtual PC, método OnMediaInsert
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883f7990de17a9d1dbb21db9651e0f5ad4ec74aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930302"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>Método IVMDVDDriveEvents:: OnMediaInsert

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recebe a notificação de que a mídia foi inserida na unidade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mediaPath* \[ no\]
</dt> <dd>

A letra da unidade do host, ou caminho, para a imagem ISO.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é chamado quando a mídia (uma imagem ISO ou um disco em uma unidade de host) é inserida. O programa cliente deve implementar esse método de interface para receber a notificação do \_ evento vmDVDDriveEvent OnInsert originado do [**IVMDVDDrive**](ivmdvddrive.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents é definido como c2a7d8e9-E76C-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

