---
title: Propriedade OSMinorVersion de IVMGuestOS (VPCCOMInterfaces.h)
description: A versão secundária do sistema operacional convidado em execução na máquina virtual.
ms.assetid: fa71e215-8633-4f53-ab71-bc9bfdb56cc8
keywords:
- Propriedade OSMinorVersion Pc Virtual
- Propriedade OSMinorVersion Pc Virtual , interface IVMGuestOS
- INTERFACE IVMGuestOS PC Virtual, propriedade OSMinorVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMinorVersion
- IVMGuestOS.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed509994c4105aeeb90f704b32f3e6bb10e9ad70791e607ebbae7db713ec60dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472536"
---
# <a name="ivmguestososminorversion-property"></a>Propriedade IVMGuestOS::OSMinorVersion

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a versão secundária do sistema operacional convidado em execução na máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_OSMinorVersion(
  [out, retval] BSTR *minorVersion
);
```



## <a name="property-value"></a>Valor da propriedade

A versão secundária.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                        |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                            | O parâmetro é **NULL.**<br/>                           |
| <dl> <dt>VM \_ E \_ VM \_ NÃO \_ EXECUTANDO</dt> <dt>0XA0040206</dt> </dl>               | A VM não está em execução.<br/>                               |
| <dl> <dt>VM \_ O \_ RECURSO DE ADIÇÕES DO E \_ NÃO \_ \_ É</dt> <dt>0XA0040505</dt> </dl> | Os componentes de integração não estão instalados nessa VM.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS é definido como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

