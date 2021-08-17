---
title: WM_GETOBJECT mensagem (Winuser.h)
description: Enviado por Microsoft Active Accessibility e microsoft Automação da Interface do Usuário para obter informações sobre um objeto acessível contido em um aplicativo de servidor.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- WM_GETOBJECT mensagem Windows Acessibilidade
topic_type:
- apiref
api_name:
- WM_GETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2767a689b87c2e293cb481647c61a29ad40167992e637802d1c0be63d18fc74e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744732"
---
# <a name="wm_getobject-message"></a>Mensagem \_ WM GETOBJECT

Enviado por Microsoft Active Accessibility e microsoft Automação da Interface do Usuário para obter informações sobre um objeto acessível contido em um aplicativo de servidor.

Os aplicativos nunca enviam essa mensagem diretamente. Microsoft Active Accessibility envia essa mensagem em resposta a chamadas [**para AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow). No entanto, os aplicativos de servidor lidam com essa mensagem. Automação da Interface do Usuário envia essa mensagem em resposta a chamadas para [**IUIAutomation::ElementFromHandle,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e ao manipular eventos para os quais um cliente se registrou.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* 
</dt> <dd>

Fornece informações adicionais sobre a mensagem e é usada somente pelo sistema. Os servidores *passam dwFlags* como o *parâmetro wParam* na chamada para [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) ao manipular a mensagem.

</dd> <dt>

*dwObjId* 
</dt> <dd>

Identificador de objeto. Esse valor é uma das constantes [do identificador de](object-identifiers.md) objeto ou um identificador de objeto personalizado. Um aplicativo de servidor deve verificar esse valor para identificar o tipo de informação que está sendo solicitado. Antes de comparar esse valor com os valores OBJID, o servidor deve castiá-lo para DWORD; caso contrário, em um Windows de 64 bits, a extensão de sinal do \_ *lParam* pode interferir na comparação. 

-   Se *dwObjId* for um dos valores OBJID como OBJID CLIENT , a solicitação será para um objeto Microsoft Active Accessibility que implementa \_ [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). [**\_**](object-identifiers.md)
-   Se *dwObjId* for igual a **UiaRootObjectId**, a solicitação será para um Automação da Interface do Usuário provedor. Se o servidor estiver implementando Automação da Interface do Usuário, ele deverá retornar um provedor usando a [**função UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)
-   Se *dwObjId* for [**OBJID \_ NATIVEOM**](object-identifiers.md), a solicitação será para o modelo de objeto subjacente do controle. Se o controle for compatível com essa solicitação, ele deverá retornar uma interface COM apropriada chamando a [**função LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
-   Se *dwObjId* for [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md), a solicitação será para que o controle se identifique como um controle Windows padrão ou um controle comum implementado pela biblioteca de controle comum (ComCtrl.dll).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a janela ou o controle não precisar responder a essa mensagem, ele deverá passar a mensagem para a [**função DefWindowProc;**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) caso contrário, a janela ou controle deverá retornar um valor que corresponda à solicitação especificada por *dwObjId*:

-   Se a janela ou o controle Automação da Interface do Usuário, a janela ou controle deverá retornar o valor obtido por uma chamada para a [**função UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)
-   Se *dwObjId* for [**OBJID \_ NATIVEOM**](object-identifiers.md) e a janela expor um Modelo de Objeto nativo, as janelas deverão retornar o valor obtido por uma chamada para a [**função LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
-   Se *dwObjId* for [**OBJID \_ CLIENT**](object-identifiers.md) e a janela implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), a janela deverá retornar o valor obtido por uma chamada para a [**função LresultFromObject.**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)

## <a name="remarks"></a>Comentários

Quando um cliente chama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou qualquer uma das outras funções **AccessibleObjectFrom**_X_ que recuperam uma interface para um objeto, o Microsoft Active Accessibility envia a mensagem **WM \_ GETOBJECT** para o procedimento de janela apropriado dentro do aplicativo de servidor apropriado. Durante o processamento **de WM \_ GETOBJECT,** os aplicativos de servidor chamam [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) e usam o valor de retorno dessa função como o valor de retorno da mensagem. Microsoft Active Accessibility, em conjunto com a biblioteca COM, executa o marshaling apropriado e passa o ponteiro de interface do servidor de volta para o cliente.

Os servidores não respondem **ao WM \_ GETOBJECT** antes que o objeto seja totalmente inicializado ou depois de começar a fechar. Quando um aplicativo cria uma nova janela, o sistema envia [**EVENT \_ OBJECT \_ CREATE**](event-constants.md) para notificar os clientes antes de enviar a mensagem [WM \_ CREATE](../winmsg/wm-create.md) para o procedimento de janela do aplicativo. Como muitos aplicativos usam WM CREATE para iniciar o processo de inicialização, os servidores não respondem à mensagem \_ **WM \_ GETOBJECT** até que o processamento da **mensagem WM \_ CREATE** seja concluído.

Um servidor usa **WM \_ GETOBJECT** para executar as seguintes tarefas:

-   [Criar novos objetos acessíveis](create-new-accessible-objects.md)
-   [Reutilizar ponteiros existentes para objetos](reuse-existing-pointers-to-objects.md)
-   [Criar novas interfaces para o mesmo objeto](create-new-interfaces-to-the-same-object.md)

Para clientes, isso significa que eles podem receber ponteiros de interface distintos para o mesmo elemento de interface do usuário, dependendo da ação do servidor. Para determinar se dois ponteiros de interface apontam para o mesmo elemento de interface do usuário, os clientes comparam as propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto. Comparar ponteiros não funciona.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Redistribuível<br/>          | Acessibilidade Ativa 1.3 RDK no Windows NT 4.0 com SP6 e posterior e Windows 95<br/>              |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como lidar com WM \_ GETOBJECT](how-to-handle-wm-getobject.md)
</dt> <dt>

[Como o WM \_ GETOBJECT funciona](how-wm-getobject-works.md)
</dt> <dt>

[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

