---
description: Fornece dados para um evento de suspensão de aplicativo.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interface ISuspendingEventArgs (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751572"
---
# <a name="isuspendingeventargs-interface"></a>Interface ISuspendingEventArgs

Fornece dados para um evento de suspensão de aplicativo.

## <a name="members"></a>Membros

A interface **ISuspendingEventArgs** herda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingEventArgs** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **ISuspendingEventArgs** tem essas propriedades.



| Propriedade                                                                           | Tipo de acesso           | Descrição                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**SuspendingOperation**](isuspendingeventargs-suspendingoperation.md)<br/> | Leitura/gravação<br/> | Obtém a operação de suspensão do aplicativo.<br/> |



 

## <a name="remarks"></a>Comentários

Esse objeto é acessado quando você implementa manipuladores de eventos como [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)e [**adiciona \_ suspensão**](/previous-versions//hh438376(v=vs.85)) para responder a eventos de suspensão do aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| parâmetro<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 
