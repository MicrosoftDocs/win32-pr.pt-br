---
title: Método IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces. h)
description: Libera um dispositivo USB de uma máquina virtual.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- DetachUSBDevice do método virtual PC
- Método DetachUSBDevice Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, método DetachUSBDevice
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
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794596"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a>IVMVirtualMachine: método etachUSBDevice de:D

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libera um dispositivo USB de uma máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inUSBDevice* \[ no\]
</dt> <dd>

Um ponteiro [**IVMUSBDevice**](ivmusbdevice.md) que representa o dispositivo USB a ser desanexado da máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                          | Descrição                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | A operação foi bem-sucedida.<br/>       |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                  | O parâmetro é **NULL**.<br/>          |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>     | A máquina virtual não está em execução.<br/> |
| <dl> <dt>**VM \_ \_ \_ \_ Falha de desanexação de USB E**</dt> <dt>0xA00400927</dt> </dl> | Falha na operação de desanexação.<br/>        |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>          | Ocorreu um erro inesperado.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

