---
title: Propriedade IVMTask ErrorDescription (VPCCOMInterfaces. h)
description: Recupera a descrição de erro localizada registrada para esta tarefa.
ms.assetid: 85728775-14b6-4031-9ccd-4c4f8c410705
keywords:
- Propriedade ErrorDescription Virtual PC
- Propriedade ErrorDescription Virtual PC, interface IVMTask
- IVMTask interface virtual PC, Propriedade ErrorDescription
topic_type:
- apiref
api_name:
- IVMTask.ErrorDescription
- IVMTask.get_ErrorDescription
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d59df4aec21facae522fa4cb734bbd99090dc850ad840baab0be9f53ecf0c64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123331"
---
# <a name="ivmtaskerrordescription-property"></a>Propriedade IVMTask:: ErrorDescription

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a descrição de erro localizada registrada para esta tarefa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ErrorDescription(
  [out, retval] BSTR *outErrorDesc
);
```



## <a name="property-value"></a>Valor da propriedade

A descrição do erro.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                    | Significado                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>         | O valor do parâmetro é **NULL**.<br/>  |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

