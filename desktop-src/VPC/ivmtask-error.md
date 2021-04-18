---
title: Propriedade de erro IVMTask (VPCCOMInterfaces. h)
description: Recupera o erro registrado para esta tarefa.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Propriedade de erro PC virtual
- Propriedade de erro Virtual PC, interface IVMTask
- Virtual PC de interface IVMTask, Propriedade Error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788869"
---
# <a name="ivmtaskerror-property"></a>Propriedade IVMTask:: Error

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o erro registrado para esta tarefa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a>Valor da propriedade

O erro registrado.

## <a name="error-codes"></a>Códigos do Erro

As instâncias de [**IVMTask**](ivmtask.md) retornadas por outras interfaces podem retornar valores adicionais. Para obter detalhes, consulte a documentação dos métodos que retornam uma instância de **IVMTask** .



| Nome/valor                                                                                                                                                                        | Significado                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                           | A operação foi bem-sucedida.<br/>                              |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                             | O valor do parâmetro é **NULL**.<br/>                           |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                     | Ocorreu um erro inesperado.<br/>                          |
| <dl> <dt>VM \_ E \_ VMVIRTUALPC \_ \_ versão mais antiga</dt> <dt>0xA0040952</dt> </dl>     | O Virtual PC 2007 e o Windows Virtual PC estão instalados.<br/> |
| <dl> <dt>VM \_ E \_ outros 0xA0040953 de \_ \_ software de virtualização</dt> <dt></dt> </dl> | Outros softwares de virtualização estão instalados.<br/>                |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

