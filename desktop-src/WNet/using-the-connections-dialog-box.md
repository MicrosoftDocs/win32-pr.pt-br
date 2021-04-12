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
# <a name="using-the-connections-dialog-box"></a><span data-ttu-id="c89be-103">Usando a caixa de diálogo conexões</span><span class="sxs-lookup"><span data-stu-id="c89be-103">Using the Connections Dialog Box</span></span>

<span data-ttu-id="c89be-104">A função [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) cria uma caixa de diálogo que permite ao usuário procurar e se conectar aos recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="c89be-104">The [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) function creates a dialog box that allows the user to browse and connect to network resources.</span></span> <span data-ttu-id="c89be-105">Você também pode chamar a função [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) para criar uma caixa de diálogo conexões.</span><span class="sxs-lookup"><span data-stu-id="c89be-105">You can also call the [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) function to create a connections dialog box.</span></span> <span data-ttu-id="c89be-106">**WNetConnectionDialog1** requer uma estrutura [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .</span><span class="sxs-lookup"><span data-stu-id="c89be-106">**WNetConnectionDialog1** requires a [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) structure.</span></span>

<span data-ttu-id="c89be-107">A função [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) cria uma caixa de diálogo que permite ao usuário se desconectar dos recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="c89be-107">The [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) function creates a dialog box that allows the user to disconnect from network resources.</span></span>

<span data-ttu-id="c89be-108">O exemplo de código a seguir demonstra como chamar a função **WNetConnectionDialog** para criar uma caixa de diálogo que exibe recursos de disco.</span><span class="sxs-lookup"><span data-stu-id="c89be-108">The following code sample demonstrates how to call the **WNetConnectionDialog** function to create a dialog box that displays disk resources.</span></span> <span data-ttu-id="c89be-109">Se a chamada falhar, o exemplo chamará um manipulador de erro definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c89be-109">If the call fails, the sample calls an application-defined error handler.</span></span>


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



<span data-ttu-id="c89be-110">Para obter mais informações sobre como usar um manipulador de erro definido pelo aplicativo, consulte [recuperando erros de rede](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c89be-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 