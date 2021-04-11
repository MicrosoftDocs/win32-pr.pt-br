---
title: Propriedade de teclado IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o dispositivo de teclado para a máquina virtual.
ms.assetid: bf516d07-eea9-40e3-b0d3-0fd4d3a04eb1
keywords:
- Propriedade de teclado virtual PC
- Propriedade de teclado virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade Keyboard
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Keyboard
- IVMVirtualMachine.get_Keyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31080b376a9e0fa999d568e5f3c7524d597aa0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295862"
---
# <a name="ivmvirtualmachinekeyboard-property"></a>Propriedade IVMVirtualMachine:: Keyboard

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o dispositivo de teclado para a máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Keyboard(
  [out, retval] IVMKeyboard **keyboard
);
```



## <a name="property-value"></a>Valor da propriedade

O objeto [**IVMKeyboard**](ivmkeyboard.md) .

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

 

