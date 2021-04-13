---
title: Propriedade IVMHardDiskConnection HD (VPCCOMInterfaces. h)
description: Recupera um objeto de disco rígido correspondente a esta conexão.
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- Propriedade HD Virtual PC
- Propriedade HD Virtual PC, interface IVMHardDiskConnection
- IVMHardDiskConnection interface virtual PC, Propriedade HD
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
ms.openlocfilehash: 9baa365606b71b693dd841471d50a475a42677d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369716"
---
# <a name="ivmharddiskconnectionharddisk-property"></a>Propriedade IVMHardDiskConnection:: HD

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera um objeto de disco rígido correspondente a esta conexão.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**IVMHardDisk**](ivmharddisk.md) que descreve o disco rígido associado a essa conexão.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                       | Significado                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                          | A operação foi bem-sucedida.<br/>                                                                                                    |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>            | O parâmetro é **nulo** ou não é válido.<br/>                                                                                          |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>    | A configuração atual da máquina virtual não é válida.<br/>                                                                          |
| <dl> <dt>VM \_ Unidade E 0xA0040502 \_ \_ inválidas</dt> <dt></dt> </dl> | O local do barramento desta conexão não foi inicializado corretamente ou o dispositivo neste local não é um disco rígido válido.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>    | Ocorreu um erro inesperado.<br/>                                                                                                |



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

 

