---
title: Propriedade Tarefas IVMVirtualPC (VPCCOMInterfaces.h)
description: Recupera uma coleção de tarefas.
ms.assetid: bba9c4b4-c933-43c8-9fbc-f2beb59867cf
keywords:
- Propriedade Tarefas PC Virtual
- Propriedade Tarefas Pc Virtual , interface IVMVirtualPC
- INTERFACE IVMVirtualPC pc virtual, propriedade Tasks
topic_type:
- apiref
api_name:
- IVMVirtualPC.Tasks
- IVMVirtualPC.get_Tasks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03e0992ff177f33c1f47ac78d0ffec94d59c330b810a796aa78530b9092b71e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056534"
---
# <a name="ivmvirtualpctasks-property"></a>Propriedade IVMVirtualPC::Tasks

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma coleção de tarefas.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Tasks(
  [out, retval] IVMTaskCollection **taskCollection
);
```



## <a name="property-value"></a>Valor da propriedade

Uma coleção de [**objetos IVMTask.**](ivmtask.md) Consulte [**IVMTaskCollection**](ivmtaskcollection.md).

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                           | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                                | O parâmetro é **NULL.**<br/>                                                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>VM \_ VIRTUALIZAÇÃO \_ DE HARDWARE E \_ \_ DESABILITADA</dt> <dt>0XA0040951</dt> </dl> | O processador não dá suporte a extensões de HAV (Virtualização Acelerada de Hardware).<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

