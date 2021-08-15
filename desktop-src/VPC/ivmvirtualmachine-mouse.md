---
title: Propriedade de mouse IVMVirtualMachine (VPCCOMInterfaces.h)
description: Recupera o dispositivo do mouse para a máquina virtual.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Propriedade do mouse Pc Virtual
- Propriedade do mouse Pc Virtual, interface IVMVirtualMachine
- INTERFACE IVMVirtualMachine pc virtual , propriedade mouse
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
ms.openlocfilehash: 96ef16d32410e66e8ea3a3baf23160074cf99d97762df3402bf437d0719d6332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344650"
---
# <a name="ivmvirtualmachinemouse-property"></a>Propriedade IVMVirtualMachine::Mouse

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o dispositivo do mouse para a máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a>Valor da propriedade

Um [**objeto IVMMouse.**](ivmmouse.md)

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                         | Significado                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | A operação foi bem-sucedida.<br/>       |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>              | O parâmetro é **NULL.**<br/>          |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>      | A configuração é desconhecida.<br/>       |
| <dl> <dt>VM \_ E \_ VM \_ NÃO \_ EXECUTANDO</dt> <dt>0XA0040206</dt> </dl> | A máquina virtual não está em execução.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Ocorreu um erro inesperado.<br/>   |



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

 

