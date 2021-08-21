---
description: As \_ constantes LINEINITIALIZEEXOPTION especificam qual mecanismo de notificação de eventos usar ao inicializar uma sessão.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Constantes de LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a1df7c4ea88cad126dcf5b542dbbdc33704814518dbc79cdf5d6bff5da402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073036"
---
# <a name="lineinitializeexoption_-constants"></a>\_Constantes LINEINITIALIZEEXOPTION

As **constantes \_ LINEINITIALIZEEXOPTION** especificam qual mecanismo de notificação de eventos usar ao inicializar uma sessão.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



O aplicativo deseja usar o mecanismo de notificação de evento de controle do hub de chamadas. Essa constante é exposta somente a aplicativos que negociam uma versão TAPI do 3,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**
</dt> <dd> <dl> <dt>



O aplicativo deseja usar o mecanismo de notificação de eventos da porta de conclusão. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**
</dt> <dd> <dl> <dt>



O aplicativo deseja usar o mecanismo de notificação de eventos do manipulador de eventos. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**
</dt> <dd> <dl> <dt>



O aplicativo deseja usar o mecanismo de notificação de eventos de janela oculta. Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Consulte [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) para obter mais detalhes sobre a operação dessas opções.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




