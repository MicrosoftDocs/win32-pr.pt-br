---
title: Propriedade de _NewEnum IVMSerialPortCollection (VPCCOMInterfaces.h)
description: Recupera um enumerador para a coleção. | IvMSerialPortCollection _NewEnum propriedade (VPCCOMInterfaces.h)
ms.assetid: 4bf7bbde-d97f-424e-afa0-ff0e334740b5
keywords:
- _NewEnum propriedade Virtual PC
- _NewEnum propriedade Virtual PC , interface IVMSerialPortCollection
- Interface IVMSerialPortCollection do COMPUTADOR Virtual , _NewEnum propriedade
topic_type:
- apiref
api_name:
- IVMSerialPortCollection._NewEnum
- IVMSerialPortCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc18308b63bfb3728769dead8e2e5e9368f974a6fc01c10fd90123fdfb06788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118843903"
---
# <a name="ivmserialportcollection_newenum-property"></a>IVMSerialPortCollection:: \_ propriedade NewEnum

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
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é NULL.<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection é definido como dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMSerialPortCollection**](ivmserialportcollection.md)
</dt> </dl>

 

