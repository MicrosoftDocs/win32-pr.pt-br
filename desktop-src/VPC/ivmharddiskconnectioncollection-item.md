---
title: Propriedade item IVMHardDiskConnectionCollection (VPCCOMInterfaces.h)
description: Recupera o objeto de conexão de disco rígido que corresponde ao índice especificado.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Propriedade de item PC virtual
- Propriedade de item Pc Virtual, interface IVMHardDiskConnectionCollection
- INTERFACE IVMHardDiskConnectionCollection pc virtual , propriedade Item
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c829d7294925b7f95f8229779ca91e04ce305125d787acad14c8dd7cd9cff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974306"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a>Propriedade IVMHardDiskConnectionCollection::Item

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o objeto de conexão de disco rígido que corresponde ao índice especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a>Valor da propriedade

O [**objeto IVMHardDiskConnection.**](ivmharddiskconnection.md)

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida. <br/>                                                      |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O *parâmetro hardDiskConnection* é **NULL.** <br/>                                    |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | O índice do item solicitado não corresponde a um item nesta coleção. <br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | A configuração é desconhecida.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/>                                                   |



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

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

