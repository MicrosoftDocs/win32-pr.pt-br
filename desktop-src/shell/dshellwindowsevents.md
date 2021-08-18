---
description: Recebe eventos de registro de janela do IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Objeto DShellWindowsEvents (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 13335268b892e4ac95520221fcd2e413c9c255225ccd8fc36c3c73cbf8c327a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009536"
---
# <a name="dshellwindowsevents-object"></a>Objeto DShellWindowsEvents

Recebe eventos [**de registro de janela do IShellWindows.**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows)

## <a name="members"></a>Membros

O **objeto DShellWindowsEvents** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O **objeto DShellWindowsEvents** tem esses métodos.



| Método                                                           | Descrição                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | Chamado quando uma janela é registrada como uma janela do Shell. <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | Chamado quando o registro de uma janela do Shell é revogado. <br/> |



 

## <a name="remarks"></a>Comentários

Use **DShellWindowsEvents** para monitorar quando uma janela do Shell é registrada ou revogada. Para obter mais informações, consulte [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Produto<br/> | Internet Explorer 5<br/>                                                                                           |
| Cabeçalho<br/>  | <dl> <dt>Exdisp.h</dt> </dl>                                      |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (versão 5.00.2014.0216 ou posterior)</dt> </dl> |
| IID<br/>     | IID \_ IShellWindows<br/>                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




