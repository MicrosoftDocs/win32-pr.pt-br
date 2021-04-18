---
title: Propriedade IVMDVDDrive BusNumber (VPCCOMInterfaces. h)
description: Recupera o número do barramento ao qual este dispositivo está anexado.
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- Propriedade BusNumber Virtual PC
- Propriedade BusNumber Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, Propriedade BusNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789729"
---
# <a name="ivmdvddrivebusnumber-property"></a>Propriedade IVMDVDDrive:: BusNumber

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número do barramento ao qual este dispositivo está anexado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>Valor da propriedade

O número do barramento. Por exemplo, em um barramento IDE, esse valor representaria o local primário ou secundário.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                       | Significado                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | A operação foi bem-sucedida.<br/>                                          |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>            | O parâmetro é **NULL**.<br/>                                             |
| <dl> <dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt> </dl> | O local do barramento desta unidade de DVD não foi inicializado corretamente.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>    | Ocorreu um erro inesperado.<br/>                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

