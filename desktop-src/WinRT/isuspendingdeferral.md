---
description: Gerencia uma operação de suspensão de aplicativo atrasada.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interface ISuspendingDeferral (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749524"
---
# <a name="isuspendingdeferral-interface"></a>Interface ISuspendingDeferral

Gerencia uma operação de suspensão de aplicativo atrasada.

## <a name="members"></a>Membros

A interface **ISuspendingDeferral** herda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingDeferral** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISuspendingDeferral** tem esses métodos.



| Método                                           | Descrição                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Concluir**](isuspendingdeferral-complete.md) | Notifica o sistema que o aplicativo salvou seus dados e está pronto para ser suspenso.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 
