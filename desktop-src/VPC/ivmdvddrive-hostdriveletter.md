---
title: Propriedade IvMDVDDrive HostDriveLetter (VPCCOMInterfaces.h)
description: A letra do conjunto de unidade de host para este dispositivo.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Propriedade HostDriveLetter Pc Virtual
- Propriedade HostDriveLetter Pc Virtual , interface IVMDVDDrive
- INTERFACE IVMDVDDrive Pc Virtual , propriedade HostDriveLetter
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eb9105ec970331a755881d7f5b1425cf43c58f5267f5970042ce64b458070a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056864"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>Propriedade IVMDVDDrive::HostDriveLetter

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a letra do conjunto de unidade de host para este dispositivo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a>Valor da propriedade

A letra da unidade.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                            | Significado                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | A operação foi bem-sucedida.<br/>                             |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                 | O parâmetro é **NULL.**<br/>                                |
| <dl> <dt>E \_ FAIL</dt> <dt>0X80004005</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                         |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>         | Não foi possível encontrar a máquina virtual.<br/>                   |
| <dl> <dt>VM \_ E \_ MEDIA WRONG TYPE \_ \_ 0XA00400728</dt> <dt></dt> </dl> | A mídia capturada por essa unidade de DVD não é uma unidade de host.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Ocorreu um erro inesperado.<br/>                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDVDDrive é definido como \_ b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

