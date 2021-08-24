---
title: IVMHardDiskConnectionCollection _NewEnum propriedade (VPCCOMInterfaces.h)
description: Recupera um enumerador para a coleção. | IVMHardDiskConnectionCollection _NewEnum propriedade (VPCCOMInterfaces.h)
ms.assetid: 9302f536-de25-4aac-88cf-9f4af6efcda7
keywords:
- _NewEnum propriedade Virtual PC
- _NewEnum propriedade Virtual PC , interface IVMHardDiskConnectionCollection
- INTERFACE IVMHardDiskConnectionCollection pc virtual , _NewEnum propriedade
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection._NewEnum
- IVMHardDiskConnectionCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02c4bbd5d0d54d5116adc09c3a0a23c4594834b48b1b28d1700d41e5525b5d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510796"
---
# <a name="ivmharddiskconnectioncollection_newenum-property"></a>IVMHardDiskConnectionCollection:: \_ propriedade NewEnum

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
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                          |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                               |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection é definido como b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

