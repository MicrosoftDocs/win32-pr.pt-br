---
description: Fornece informações sobre uma operação de suspensão de aplicativo.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interface ISuspendingOperation (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: f17cd3d3b1eab67d0abfea200e657d8c4a17d8df9e3bb850e4ea361a760d19df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758626"
---
# <a name="isuspendingoperation-interface"></a>Interface ISuspendingOperation

Fornece informações sobre uma operação de suspensão de aplicativo.

## <a name="members"></a>Membros

A interface **ISuspendingOperation** herda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingOperation** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **ISuspendingOperation** tem esses métodos.



| Método                                                  | Descrição                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**Getadiamento**](isuspendingoperation-getdeferral.md) | Solicita que a operação de suspensão do aplicativo seja atrasada.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **ISuspendingOperation** tem essas propriedades.



| Propriedade                                                     | Tipo de acesso           | Descrição                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Prazo**](isuspendingoperation-deadline.md)<br/> | Leitura/gravação<br/> | Obtém o tempo restante antes de uma operação de suspensão de aplicativo atrasado continuar.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 
