---
title: Propriedade IvMVirtualPC MinimumMemoryPerVM (VPCCOMInterfaces.h)
description: Recupera a quantidade mínima de memória física por máquina virtual, em megabytes.
ms.assetid: 3e7757cd-df45-4b30-9a38-6cfca0ee631a
keywords:
- Propriedade MinimumMemoryPerVM Pc Virtual
- Propriedade MinimumMemoryPerVM pc virtual , interface IVMVirtualPC
- INTERFACE IVMVirtualPC Pc Virtual , propriedade MinimumMemoryPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MinimumMemoryPerVM
- IVMVirtualPC.get_MinimumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35c33637bf79fc2600921914b189803970580c7554075ff8b09c026d03814ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136539"
---
# <a name="ivmvirtualpcminimummemorypervm-property"></a>Propriedade IVMVirtualPC::MinimumMemoryPerVM

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a quantidade mínima de memória física por máquina virtual, em megabytes.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MinimumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Valor da propriedade

A quantidade mínima aceitável, em megabytes, de memória física por máquina virtual.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                                | O parâmetro é **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA</dt> <dt>0XA0040951</dt> </dl> | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

