---
title: Mensagem de WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: A \_ mensagem CAPCONTROL de retorno de chamada do WM Cap \_ \_ \_ define uma função de retorno de chamada no aplicativo, dando a ele um controle de gravação preciso. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- mensagem de WM_CAP_SET_CALLBACK_CAPCONTROL Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e5786ef67fe66c7ad0dac463824dcd49bfb34e4c8239ddca74ed60e3861bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369514"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>WM \_ Cap \_ set \_ retorno de chamada \_ CAPCONTROL Message

A **mensagem \_ CAPCONTROL de \_ retorno de \_ chamada \_ do WM Cap** define uma função de retorno de chamada no aplicativo, dando a ele um controle de gravação preciso. Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Ponteiro para a função de retorno de chamada, do tipo [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback). Especifique **NULL** para esse parâmetro para desabilitar uma função de retorno de chamada instalada anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se houver uma sessão de captura de streaming ou de um único quadro em andamento.

## <a name="remarks"></a>Comentários

Uma única função de retorno de chamada é usada para dar ao aplicativo o controle preciso sobre o tempo de início e conclusão da captura de streaming. A janela de captura primeiro chama o procedimento com *nState* definido como CONTROLCALLBACK \_ Prevert após a alocação de todos os buffers e a conclusão de todas as outras preparações de captura. Isso permite que o aplicativo tenha a capacidade de obter fontes de vídeo, retornando da função de retorno de chamada na gravação exata do momento é começar. Um valor de retorno de **true** da função de retorno de chamada continua a captura e um valor de retorno de **false** anula a captura. Após a captura começar, essa função de retorno de chamada será chamada frequentemente com *nState* definido como CONTROLCALLBACK \_ Capture para permitir que o aplicativo encerre a captura retornando **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





