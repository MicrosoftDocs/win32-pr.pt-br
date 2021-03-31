---
title: Propriedade IVMVirtualPC USBDeviceCollection (VPCCOMInterfaces. h)
description: Uma coleção enumerável de todos os dispositivos USB conectados ao host.
ms.assetid: 80844912-15b1-44d1-8d07-dca90c579927
keywords:
- Propriedade USBDeviceCollection Virtual PC
- Propriedade USBDeviceCollection Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade USBDeviceCollection
topic_type:
- apiref
api_name:
- IVMVirtualPC.USBDeviceCollection
- IVMVirtualPC.get_USBDeviceCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0428862cdd53ef6e657624d5dbd3e15c2445042f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644784"
---
# <a name="ivmvirtualpcusbdevicecollection-property"></a>Propriedade IVMVirtualPC:: USBDeviceCollection

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma coleção enumerável de todos os dispositivos USB conectados ao host.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_USBDeviceCollection(
  [out, retval] IVMUSBDeviceCollection **usbDeviceCollection
);
```



## <a name="property-value"></a>Valor da propriedade

Uma referência a um ponteiro [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md) que representa uma coleção de objetos [**IVMUSBDevice**](ivmusbdevice.md) .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                                | Significado                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                   | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                     | O parâmetro é **NULL**.<br/>                                                           |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                             | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>VM \_ \_Falha de enumeração de USB E \_ \_ \_ mais \_ dispositivos</dt> <dt>0xA0040930</dt> </dl> | Mais de 16 dispositivos USB estão conectados ao host.<br/>                                  |
| <dl> <dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt> </dl>      | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

