---
title: Propriedade _NewEnum IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera um enumerador para a coleção de CD/DVD.
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- _NewEnum a propriedade Virtual PC
- Propriedade _NewEnum Virtual PC, interface IVMDVDDriveCollection
- IVMDVDDriveCollection interface virtual PC, Propriedade _NewEnum
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfd0de3aaf6b25808d1afa591b0c2099599e6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918401"
---
# <a name="ivmdvddrivecollection_newenum-property"></a>Propriedade IVMDVDDriveCollection:: \_ NewEnum

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera um enumerador para a coleção de CD/DVD.

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



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>E \_ FALHA</dt> <dt>0x80004005</dt> </dl>            | Ocorreu um erro inesperado.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Erro inesperado.<br/>     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection é definido como bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDriveCollection**](ivmdvddrivecollection.md)
</dt> </dl>

 

