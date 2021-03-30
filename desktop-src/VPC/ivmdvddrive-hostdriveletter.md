---
title: Propriedade IVMDVDDrive HostDriveLetter (VPCCOMInterfaces. h)
description: A letra da unidade do host definida para este dispositivo.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- Propriedade HostDriveLetter Virtual PC
- Propriedade HostDriveLetter Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, Propriedade HostDriveLetter
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
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644548"
---
# <a name="ivmdvddrivehostdriveletter-property"></a>Propriedade IVMDVDDrive:: HostDriveLetter

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a letra do conjunto de unidades do host para este dispositivo.

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
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                 | O parâmetro é **NULL**.<br/>                                |
| <dl> <dt>E \_ FALHA</dt> <dt>0x80004005</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                         |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>         | Não foi possível encontrar a máquina virtual.<br/>                   |
| <dl> <dt>VM \_ \_Mídia E \_ \_ tipo incorreto</dt> <dt>0xA00400728</dt> </dl> | A mídia capturada por esta unidade de DVD não é uma unidade host.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>         | Ocorreu um erro inesperado.<br/>                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

