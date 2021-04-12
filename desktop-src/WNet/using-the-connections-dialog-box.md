---
title: Usando a caixa de diálogo conexões
description: A função WNetConnectionDialog cria uma caixa de diálogo que permite ao usuário procurar e se conectar aos recursos de rede.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294242"
---
# <a name="using-the-connections-dialog-box"></a>Usando a caixa de diálogo conexões

A função [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) cria uma caixa de diálogo que permite ao usuário procurar e se conectar aos recursos de rede. Você também pode chamar a função [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) para criar uma caixa de diálogo conexões. **WNetConnectionDialog1** requer uma estrutura [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .

A função [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) cria uma caixa de diálogo que permite ao usuário se desconectar dos recursos de rede.

O exemplo de código a seguir demonstra como chamar a função **WNetConnectionDialog** para criar uma caixa de diálogo que exibe recursos de disco. Se a chamada falhar, o exemplo chamará um manipulador de erro definido pelo aplicativo.


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).

 

 