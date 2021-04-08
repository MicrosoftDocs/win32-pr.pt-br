---
title: Propriedade de item IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Recupera o objeto da unidade de CD ou DVD que corresponde ao índice especificado.
ms.assetid: ecc94eea-9ddc-46c8-87e2-e67aca83eecc
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMDVDDriveCollection
- IVMDVDDriveCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection.Item
- IVMDVDDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cc631ab6d4de3ab65071bf2b8692236f3ae03ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009328"
---
# <a name="ivmdvddrivecollectionitem-property"></a>Propriedade IVMDVDDriveCollection:: item

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o objeto da unidade de CD ou DVD que corresponde ao índice especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Item(
  [in]          long        index,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="property-value"></a>Valor da propriedade

O objeto [**IVMDVDDrive**](ivmdvddrive.md) .

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida. <br/>                                                      |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>                                                          |
| <dl> <dt>E \_ FALHA</dt> <dt>0x80004005</dt> </dl>            | Ocorreu um erro inesperado.<br/>                                                   |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | O índice do item solicitado não corresponde a um item nesta coleção. <br/> |
| <dl> <dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt> </dl> | A configuração é desconhecida.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                                                   |



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

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMDVDDriveCollection**](ivmdvddrivecollection.md)
</dt> </dl>

 

