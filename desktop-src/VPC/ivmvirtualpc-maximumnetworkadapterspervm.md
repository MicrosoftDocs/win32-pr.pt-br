---
title: Propriedade MaximumNetworkAdaptersPerVM de IVMVirtualPC (VPCCOMInterfaces.h)
description: Número máximo de interfaces de redes por máquina virtual.
ms.assetid: 92da4958-5a67-422e-a6bd-68cabf1835ab
keywords:
- Propriedade MaximumNetworkAdaptersPerVM Pc Virtual
- Propriedade MaximumNetworkAdaptersPerVM pc virtual, interface IVMVirtualPC
- INTERFACE IVMVirtualPC Pc Virtual , propriedade MaximumNetworkAdaptersPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumNetworkAdaptersPerVM
- IVMVirtualPC.get_MaximumNetworkAdaptersPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d71098da6f5f25013d4a5312c37a990d5c77da5a0bfdedd8f3888ae4b752acd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842772"
---
# <a name="ivmvirtualpcmaximumnetworkadapterspervm-property"></a>Propriedade IVMVirtualPC::MaximumNetworkAdaptersPerVM

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número máximo de interfaces de redes por máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MaximumNetworkAdaptersPerVM(
  [out, retval] long *maxNetworkAdapters
);
```



## <a name="property-value"></a>Valor da propriedade

O número máximo de interfaces de rede por máquina virtual.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                                | O parâmetro é **NULL.**<br/>                                                           |
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

 

