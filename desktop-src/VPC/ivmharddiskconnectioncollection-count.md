---
title: Propriedade IvMHardDiskConnectionCollection Count (VPCCOMInterfaces.h)
description: Recupera o número de conexões de disco rígido nesta coleção.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Propriedade Count Pc Virtual
- Propriedade Count Pc Virtual , interface IVMHardDiskConnectionCollection
- INTERFACE IVMHardDiskConnectionCollection pc virtual , propriedade Count
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccb00cf2388db8a971f5da2f726030b3f793ac878f4a59df2646195eb41ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974316"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a>Propriedade IVMHardDiskConnectionCollection::Count

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número de conexões de disco rígido nesta coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor da propriedade

O número de conexões de disco rígido.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | A configuração é desconhecida.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/> |



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

 

