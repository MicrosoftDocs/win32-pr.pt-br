---
title: Propriedade Manufacturerstring do IVMUSBDevice (VPCCOMInterfaces. h)
description: Recupera o nome do fabricante do dispositivo USB.
ms.assetid: 0d815887-96bf-4795-a4eb-32fb2f35c57e
keywords:
- Propriedade manufacturerstring Virtual PC
- Propriedade manufacturerstring Virtual PC, interface IVMUSBDevice
- IVMUSBDevice interface virtual PC, Propriedade Manufacturerstring
topic_type:
- apiref
api_name:
- IVMUSBDevice.ManufacturerString
- IVMUSBDevice.get_ManufacturerString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb0ec725779e4ffd18d46752f4083ad53c5b77c8392b45dc414d927b1038988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973706"
---
# <a name="ivmusbdevicemanufacturerstring-property"></a>Propriedade IVMUSBDevice:: Manufacturerstring

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o nome do fabricante do dispositivo USB.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ManufacturerString(
  [out, retval] BSTR *manufacturerName
);
```



## <a name="property-value"></a>Valor da propriedade

O nome do fabricante do dispositivo USB.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                            | Significado                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | O método foi concluído com êxito.<br/> |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl> | O parâmetro é **NULL**.<br/>         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMUSBDevice é definido como 63C1258C-5721-4070-B86B-A6CE2AFEC0B3<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMUSBDevice**](ivmusbdevice.md)
</dt> </dl>

 

