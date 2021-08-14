---
title: Método DetachUSBDevice de IVMVirtualMachine (VPCCOMInterfaces.h)
description: Libera um dispositivo USB de uma máquina virtual.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- Pc Virtual do método DetachUSBDevice
- Pc Virtual do método DetachUSBDevice, interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine pc virtual , método DetachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5b45821f56a9533ed851f6c73342fbd15801223832cf9bad9a380b3f97f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344670"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a>Método IVMVirtualMachine::D etachUSBDevice

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libera um dispositivo USB de uma máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inUSBDevice* \[ Em\]
</dt> <dd>

Um [**ponteiro IVMUSBDevice**](ivmusbdevice.md) que representa o dispositivo USB a ser desvinculado da máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                          | Descrição                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | A operação foi bem-sucedida.<br/>       |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                  | O parâmetro é **NULL.**<br/>          |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>     | A máquina virtual não está em execução.<br/> |
| <dl> <dt>**VM \_ FALHA \_ NA \_ \_ DESAGRUÇÃO**</dt> <dt>DE USB E 0XA00400927</dt> </dl> | Falha na operação de desconectação.<br/>        |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>          | Ocorreu um erro inesperado.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

