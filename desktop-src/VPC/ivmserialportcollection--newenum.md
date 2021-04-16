---
title: Propriedade _NewEnum IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera um enumerador para a coleção. | Propriedade _NewEnum IVMSerialPortCollection (VPCCOMInterfaces. h)
ms.assetid: 4bf7bbde-d97f-424e-afa0-ff0e334740b5
keywords:
- _NewEnum a propriedade Virtual PC
- Propriedade _NewEnum Virtual PC, interface IVMSerialPortCollection
- IVMSerialPortCollection interface virtual PC, Propriedade _NewEnum
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
ms.openlocfilehash: 4fdfc2b300823c674cf5d4fd8e36dffeb58f8c1b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506444"
---
# <a name="ivmserialportcollection_newenum-property"></a>Propriedade IVMSerialPortCollection:: \_ NewEnum

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera um enumerador para a coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Valor da propriedade

O enumerador [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/> |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é NULL.<br/>        |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection é definido como dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMSerialPortCollection**](ivmserialportcollection.md)
</dt> </dl>

 

