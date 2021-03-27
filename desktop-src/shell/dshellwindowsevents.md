---
description: Recebe eventos de registro da janela IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Objeto DShellWindowsEvents (exdisp. h)
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
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104970812"
---
# <a name="dshellwindowsevents-object"></a>Objeto DShellWindowsEvents

Recebe eventos de registro da janela [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .

## <a name="members"></a>Membros

O objeto **DShellWindowsEvents** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **DShellWindowsEvents** tem esses métodos.



| Método                                                           | Descrição                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | Chamado quando uma janela é registrada como uma janela de Shell. <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | Chamado quando o registro de uma janela do Shell é revogado. <br/> |



 

## <a name="remarks"></a>Comentários

Use **DShellWindowsEvents** para monitorar quando uma janela de Shell é registrada ou revogada. Para obter mais informações, consulte [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Produto<br/> | Internet Explorer 5<br/>                                                                                           |
| parâmetro<br/>  | <dl> <dt>O textdisp. h</dt> </dl>                                      |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (versão 5.00.2014.0216 ou posterior)</dt> </dl> |
| IID<br/>     | IShellWindows de IID \_<br/>                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




