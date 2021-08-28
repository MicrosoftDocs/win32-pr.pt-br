---
title: Propriedade HardDisk IVMHardDiskConnection (VPCCOMInterfaces.h)
description: Recupera um objeto de disco rígido correspondente a essa conexão.
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- Propriedade HardDisk Pc Virtual
- Propriedade HardDisk Pc Virtual, interface IVMHardDiskConnection
- INTERFACE IVMHardDiskConnection PC Virtual, propriedade HardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.HardDisk
- IVMHardDiskConnection.get_HardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e03eafb17aab0b27d8d47e142c4ba540933e6d09452d2ef705cf7e54c550829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118844813"
---
# <a name="ivmharddiskconnectionharddisk-property"></a>Propriedade IVMHardDiskConnection::HardDisk

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera um objeto de disco rígido correspondente a essa conexão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a>Valor da propriedade

Um [**objeto IVMHardDisk**](ivmharddisk.md) que descreve o disco rígido associado a essa conexão.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                       | Significado                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | A operação foi bem-sucedida.<br/>                                                                                                    |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>            | O parâmetro é **NULL** ou não é válido.<br/>                                                                                          |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>    | A configuração atual da máquina virtual não é válida.<br/>                                                                          |
| <dl> <dt>VM \_ E \_ UNIDADE \_ INVÁLIDA</dt> <dt>0XA0040502</dt> </dl> | O local do barramento para essa conexão não foi inicializado corretamente ou o dispositivo nesse local não é um disco rígido válido.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>    | Ocorreu um erro inesperado.<br/>                                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection é definido como aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

