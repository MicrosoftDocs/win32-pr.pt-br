---
title: Mensagem de WM_GETOBJECT (WinUser. h)
description: Enviado pelo Microsoft Acessibilidade Ativa e automação da interface do usuário da Microsoft para obter informações sobre um objeto acessível contido em um aplicativo de servidor.
ms.assetid: 59350aa1-1697-4110-b9a6-f30ee56c4cff
keywords:
- Acessibilidade do Windows WM_GETOBJECT mensagem
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
ms.openlocfilehash: fcac5c7f6dd8203c32b9f6f3c4eb59144cc3f8ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086484"
---
# <a name="wm_getobject-message"></a>Mensagem do WM \_ GETobject

Enviado pelo Microsoft Acessibilidade Ativa e automação da interface do usuário da Microsoft para obter informações sobre um objeto acessível contido em um aplicativo de servidor.

Os aplicativos nunca enviam essa mensagem diretamente. O Microsoft Acessibilidade Ativa envia essa mensagem em resposta a chamadas para [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow). No entanto, os aplicativos de servidor lidam com essa mensagem. A automação da interface do usuário envia essa mensagem em resposta às chamadas para [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**getconcentrouelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e ao manipular eventos para os quais um cliente se registrou.


```C++
dwFlags = (WPARAM)(DWORD) wParam;
dwObjId = (LPARAM)(DWORD) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwFlags* 
</dt> <dd>

Fornece informações adicionais sobre a mensagem e é usada somente pelo sistema. Os servidores passam *dwFlags* como o parâmetro *wParam* na chamada para [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) ao manipular a mensagem.

</dd> <dt>

*dwObjId* 
</dt> <dd>

Identificador de objeto. Esse valor é uma das constantes de [identificador de objeto](object-identifiers.md) ou um identificador de objeto personalizado. Um aplicativo de servidor deve verificar esse valor para identificar o tipo de informações que estão sendo solicitadas. Antes de comparar esse valor com os \_ valores de OBJID, o servidor deve convertê-lo em **DWORD**; caso contrário, no Windows de 64 bits, a extensão de sinal do *lParam* pode interferir na comparação.

-   Se *dwObjId* for um dos valores de OBJID \_ como [**OBJID \_ Client**](object-identifiers.md), a solicitação será para um objeto Microsoft acessibilidade ativa que implementa o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
-   Se *dwObjId* for igual a **UiaRootObjectId**, a solicitação será para um provedor de automação de interface do usuário. Se o servidor estiver implementando a automação da interface do usuário, ele deverá retornar um provedor usando a função [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Se *dwObjId* for [**OBJID \_ NATIVEOM**](object-identifiers.md), a solicitação será para o modelo de objeto subjacente do controle. Se o controle der suporte a essa solicitação, ele deverá retornar uma interface COM apropriada chamando a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Se *dwObjId* for [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md), a solicitação será para o controle se identificar como um controle padrão do Windows ou um controle comum implementado pela ComCtrl.dll (biblioteca de controle comum).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a janela ou o controle não precisar responder a essa mensagem, ele deverá passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) ; caso contrário, a janela ou o controle deve retornar um valor que corresponda à solicitação especificada por *dwObjId*:

-   Se a janela ou o controle implementar a automação da interface do usuário, a janela ou o controle deverá retornar o valor obtido por uma chamada para a função [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Se *dwObjId* for [**OBJID \_ NATIVEOM**](object-identifiers.md) e a janela expor um modelo de objeto nativo, o Windows deverá retornar o valor obtido por uma chamada para a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Se *dwObjId* for [**OBJID \_ Client**](object-identifiers.md) e a janela implementar [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), a janela deverá retornar o valor obtido por uma chamada para a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

## <a name="remarks"></a>Comentários

Quando um cliente chama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou qualquer uma das outras funções **AccessibleObjectFrom**_X_ que recuperam uma interface para um objeto, o Microsoft acessibilidade ativa envia a mensagem do **WM \_ GetObject** para o procedimento de janela apropriado no aplicativo de servidor apropriado. Ao processar o **WM \_ GetObject**, os aplicativos de servidor chamam [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) e usam o valor de retorno dessa função como o valor de retorno para a mensagem. O Microsoft Acessibilidade Ativa, em conjunto com a biblioteca COM, executa o marshaling apropriado e passa o ponteiro de interface do servidor de volta para o cliente.

Os servidores não respondem ao **WM \_ GetObject** antes que o objeto seja totalmente inicializado ou depois que ele começa a ser fechado. Quando um aplicativo cria uma nova janela, o sistema envia [**o \_ objeto \_ de evento CREATE**](event-constants.md) para notificar os clientes antes de enviar a mensagem de [ \_ criação do WM](../winmsg/wm-create.md) para o procedimento de janela do aplicativo. Como muitos aplicativos usam \_ o WM Create para iniciar o processo de inicialização, os servidores não respondem à mensagem do **WM \_ GetObject** até concluir o processamento da mensagem de **\_ criação do WM** .

Um servidor usa o **WM \_ GetObject** para executar as seguintes tarefas:

-   [Criar novos objetos acessíveis](create-new-accessible-objects.md)
-   [Reutilizar ponteiros existentes para objetos](reuse-existing-pointers-to-objects.md)
-   [Criar novas interfaces para o mesmo objeto](create-new-interfaces-to-the-same-object.md)

Para clientes, isso significa que eles podem receber ponteiros de interface distintos para o mesmo elemento de interface do usuário, dependendo da ação do servidor. Para determinar se dois ponteiros de interface apontam para o mesmo elemento de interface do usuário, os clientes comparam as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto. A comparação de ponteiros não funciona.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| Redistribuível<br/>          | Acessibilidade Ativa 1,3 RDK no Windows NT 4,0 com SP6 e posterior e Windows 95<br/>              |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como tratar o WM \_ GETobject](how-to-handle-wm-getobject.md)
</dt> <dt>

[Como o WM \_ GetObject funciona](how-wm-getobject-works.md)
</dt> <dt>

[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)
</dt> </dl>

 

