---
title: Propriedade Item IVMParallelPortCollection (VPCCOMInterfaces.h)
description: Recupera o objeto de porta paralela que corresponde ao índice especificado.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Propriedade de item PC virtual
- Propriedade de item PC virtual, interface IVMParallelPortCollection
- INTERFACE IVMParallelPortCollection pc virtual , propriedade Item
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a28aec3fbe9585185f61cc7941d5de8033b73019354ca480f72fe4b3b7be793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006996"
---
# <a name="ivmparallelportcollectionitem-property"></a>Propriedade IVMParallelPortCollection::Item

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o objeto de porta paralela que corresponde ao índice especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a>Valor da propriedade

O [**objeto IVMParallelPort.**](ivmparallelport.md)

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida. <br/>                                                      |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>         | O *parâmetro vmParallelPort* é **NULL.** <br/>                                        |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | O índice do item solicitado não corresponde a um item nesta coleção. <br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | A configuração é desconhecida.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/>                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection é definido como 27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> <dt>

[**IVMParallelPortCollection**](ivmparallelportcollection.md)
</dt> </dl>

 

