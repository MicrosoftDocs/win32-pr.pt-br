---
title: Propriedade IVMVirtualMachine FloppyDrives (VPCCOMInterfaces. h)
description: Recupera uma coleção enumerável de unidades de disquete anexadas à máquina virtual.
ms.assetid: 8b8ea1c7-77c3-46b6-ab0b-0c7b4ab387ae
keywords:
- Propriedade FloppyDrives Virtual PC
- Propriedade FloppyDrives Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade FloppyDrives
topic_type:
- apiref
api_name:
- IVMVirtualMachine.FloppyDrives
- IVMVirtualMachine.get_FloppyDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4ec942d55c3d98b3d45a013fb1142ea097edfca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794595"
---
# <a name="ivmvirtualmachinefloppydrives-property"></a>Propriedade IVMVirtualMachine:: FloppyDrives

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma coleção enumerável de unidades de disquete anexadas à máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_FloppyDrives(
  [out, retval] IVMFloppyDriveCollection **floppyCollection
);
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A configuração é desconhecida.<br/>     |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



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

 

