---
title: Propriedade IvMVirtualPC SuggestedMaximumMemoryPerVM (VPCCOMInterfaces.h)
description: Recupera a quantidade máxima permitida sugerida de memória física por máquina virtual, em megabytes, para evitar condições de memória baixas no host.
ms.assetid: 533cca40-f41d-4717-87ae-d8072414a637
keywords:
- SuggestedMaximumMemoryPerVM propriedade Pc Virtual
- SuggestedMaximumMemoryPerVM propriedade Virtual PC , interface IVMVirtualPC
- INTERFACE IVMVirtualPC Pc Virtual , propriedade SuggestedMaximumMemoryPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.SuggestedMaximumMemoryPerVM
- IVMVirtualPC.get_SuggestedMaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb2a14ad6d48c3d156ebffd6ea0c5ae6c4cd52f94790152d373fdc7cf47e118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768036"
---
# <a name="ivmvirtualpcsuggestedmaximummemorypervm-property"></a>Propriedade IVMVirtualPC::SuggestedMaximumMemoryPerVM

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a quantidade máxima permitida sugerida de memória física por máquina virtual, em megabytes, para evitar condições de memória baixas no host.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SuggestedMaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a>Valor da propriedade

A quantidade máxima permitida sugerida, em megabytes, de memória física por máquina virtual.

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

 

