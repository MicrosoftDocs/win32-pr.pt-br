---
title: Propriedade de mouse IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera o dispositivo de mouse para a máquina virtual.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Propriedade do mouse Virtual PC
- Propriedade do mouse Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade do mouse
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111d511f4e7948a83a968b154721bf81dbfe53b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813249"
---
# <a name="ivmvirtualmachinemouse-property"></a>Propriedade IVMVirtualMachine:: mouse

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o dispositivo de mouse para a máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a>Valor da propriedade

Um objeto [**IVMMouse**](ivmmouse.md) .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                         | Significado                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>       |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>              | O parâmetro é **NULL**.<br/>          |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl>      | A configuração é desconhecida.<br/>       |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl> | A máquina virtual não está em execução.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>      | Ocorreu um erro inesperado.<br/>   |



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

 

