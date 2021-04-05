---
title: Propriedade IVMHardDiskConnection DeviceNumber (VPCCOMInterfaces. h)
description: Recupera o número do dispositivo ao qual a imagem da unidade está anexada.
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- Propriedade DeviceNumber Virtual PC
- Propriedade DeviceNumber Virtual PC, interface IVMHardDiskConnection
- IVMHardDiskConnection interface virtual PC, Propriedade DeviceNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69f7d9d3f9a373c9b8086857af56c7e5da9f5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086265"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a>IVMHardDiskConnection: Propriedade eviceNumber de:D

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número do dispositivo ao qual a imagem da unidade está anexada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a>Valor da propriedade

O número do dispositivo que corresponde a essa conexão.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                       | Significado                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | A operação foi bem-sucedida.<br/>                                           |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>            | O parâmetro é **nulo** ou não é válido.<br/>                                 |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>    | A configuração atual da máquina virtual não é válida.<br/>                 |
| <dl> <dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt> </dl> | O local do barramento desta conexão não foi inicializado corretamente.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>    | Ocorreu um erro inesperado.<br/>                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection é definido como aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

