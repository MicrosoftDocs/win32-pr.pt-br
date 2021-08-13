---
title: Propriedade Count de IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Recupera o número de portas seriais nesta coleção.
ms.assetid: 94ff6c9d-17bc-4aa5-a486-d4428c829d02
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMSerialPortCollection
- Virtual PC de interface IVMSerialPortCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Count
- IVMSerialPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8c7390b4637cf8e39fe83fcbb9844913a41d20fd2ed9515695ec068b33af6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593149"
---
# <a name="ivmserialportcollectioncount-property"></a>Propriedade IVMSerialPortCollection:: Count

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o número de portas seriais nesta coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valor da propriedade

O número de portas seriais.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                            | Significado                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | A operação foi bem-sucedida.<br/> |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl> | O parâmetro é **NULL**.<br/>    |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection é definido como dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMSerialPortCollection**](ivmserialportcollection.md)
</dt> </dl>

 

