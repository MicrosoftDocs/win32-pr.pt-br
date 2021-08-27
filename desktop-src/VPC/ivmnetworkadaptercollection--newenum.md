---
title: IVMNetworkAdapterCollection _NewEnum propriedade (VPCCOMInterfaces.h)
description: Recupera um enumerador para a coleção. | IVMNetworkAdapterCollection _NewEnum propriedade (VPCCOMInterfaces.h)
ms.assetid: 9b970fc6-f8a3-4a16-9d59-789a59a99b68
keywords:
- _NewEnum propriedade Virtual PC
- _NewEnum propriedade Virtual PC , interface IVMNetworkAdapterCollection
- INTERFACE IVMNetworkAdapterCollection pc virtual , _NewEnum propriedade
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection._NewEnum
- IVMNetworkAdapterCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05924b793d281cc190eed434c70efa37f1a930e905751973a6b0285920e1aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007086"
---
# <a name="ivmnetworkadaptercollection_newenum-property"></a>IVMNetworkAdapterCollection:: \_ propriedade NewEnum

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera um enumerador para a coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Valor da propriedade

O [enumerador IEnumVARIANT.](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/> |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>    |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                           |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMNetworkAdapterCollection é definido como ebaeafe9-ebcd-47cf-866e-ad87d735e479<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)
</dt> </dl>

 

