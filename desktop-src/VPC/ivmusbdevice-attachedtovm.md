---
title: Propriedade IVMUSBDevice AttachedToVM (VPCCOMInterfaces. h)
description: Recupera o nome da máquina virtual à qual o dispositivo USB está anexado.
ms.assetid: 214ed891-1fca-4311-945a-0ce3d05d604e
keywords:
- Propriedade AttachedToVM Virtual PC
- Propriedade AttachedToVM Virtual PC, interface IVMUSBDevice
- IVMUSBDevice interface virtual PC, Propriedade AttachedToVM
topic_type:
- apiref
api_name:
- IVMUSBDevice.AttachedToVM
- IVMUSBDevice.get_AttachedToVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c64e265cba81858bc887cbf595426bffd1b604aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009436"
---
# <a name="ivmusbdeviceattachedtovm-property"></a>Propriedade IVMUSBDevice:: AttachedToVM

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o nome da máquina virtual à qual o dispositivo USB está anexado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AttachedToVM(
  [out, retval] BSTR *ConfigName
);
```



## <a name="property-value"></a>Valor da propriedade

O nome da VM (máquina virtual).

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                           | Significado                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                              | O dispositivo é anexado à VM e seu nome é retornado.<br/> |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                           | O dispositivo está conectado ao host.<br/>                         |
| <dl> <dt>VM \_ 0xA00400929 \_ \_ \_ VM externa USB</dt> <dt></dt> </dl> | O dispositivo está anexado a uma VM em outra sessão de usuário.<br/>     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                | O parâmetro é **NULL**.<br/>                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

