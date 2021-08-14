---
title: Propriedade Count IVMFloppyDriveCollection (VPCCOMInterfaces.h)
description: Número de unidades de disquete nesta coleção.
ms.assetid: d430e5ae-9782-4f88-a5a4-744e79545c7a
keywords:
- Propriedade Count Pc Virtual
- Propriedade Count Pc Virtual , interface IVMFloppyDriveCollection
- INTERFACE IVMFloppyDriveCollection pc virtual , propriedade Count
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Count
- IVMFloppyDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1688a157b4352c1d2d1eba12701633e61ae6097b358737b1c9593a8ff16d122c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594832"
---
# <a name="ivmfloppydrivecollectioncount-property"></a>Propriedade IVMFloppyDriveCollection::Count

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número de unidades de disquete nesta coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor da propriedade

O número de unidades de mídia disquete.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | A configuração é desconhecida.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection é definido como 8ba70a25-f698-4ee5-85ce-3cc93a925516<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)
</dt> </dl>

 

