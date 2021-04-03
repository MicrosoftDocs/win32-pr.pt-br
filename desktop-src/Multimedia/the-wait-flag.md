---
title: O sinalizador de espera
description: O sinalizador de espera
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- Sinalizador de MCI_WAIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006176"
---
# <a name="the-wait-flag"></a><span data-ttu-id="affa7-104">O sinalizador de espera</span><span class="sxs-lookup"><span data-stu-id="affa7-104">The Wait Flag</span></span>

<span data-ttu-id="affa7-105">Os comandos MCI geralmente retornam ao usuário imediatamente, mesmo que demore alguns minutos para concluir a ação iniciada pelo comando.</span><span class="sxs-lookup"><span data-stu-id="affa7-105">MCI commands usually return to the user immediately, even if it takes several minutes to complete the action initiated by the command.</span></span> <span data-ttu-id="affa7-106">Você pode usar o sinalizador "Wait" ( \_ espera de MCI) para direcionar o dispositivo para aguardar até que a ação solicitada seja concluída antes de retornar o controle para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="affa7-106">You can use the "wait" (MCI\_WAIT) flag to direct the device to wait until the requested action is completed before returning control to the application.</span></span>

<span data-ttu-id="affa7-107">Por exemplo, o comando de [**reprodução**](play.md) a seguir não retornará o controle para o aplicativo até que a reprodução seja concluída:</span><span class="sxs-lookup"><span data-stu-id="affa7-107">For example, the following [**play**](play.md) command will not return control to the application until the playback completes:</span></span>


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> <span data-ttu-id="affa7-108">O usuário pode cancelar uma operação de espera pressionando uma tecla Break.</span><span class="sxs-lookup"><span data-stu-id="affa7-108">The user can cancel a wait operation by pressing a break key.</span></span> <span data-ttu-id="affa7-109">Por padrão, essa chave é CTRL + BREAK.</span><span class="sxs-lookup"><span data-stu-id="affa7-109">By default, this key is CTRL+BREAK.</span></span> <span data-ttu-id="affa7-110">Os aplicativos podem redefinir essa chave usando o comando [**Break**](break.md) ([**MCI \_ Break**](mci-break.md)).</span><span class="sxs-lookup"><span data-stu-id="affa7-110">Applications can redefine this key by using the [**break**](break.md) ([**MCI\_BREAK**](mci-break.md)) command.</span></span> <span data-ttu-id="affa7-111">(**A \_ interrupção do MCI** usa a estrutura de [**parâmetros de \_ interrupção \_ do MCI**](mci-break-parms.md) .) Quando uma operação de espera é cancelada, o MCI tenta retornar o controle ao aplicativo sem interromper o comando associado ao sinalizador "Wait".</span><span class="sxs-lookup"><span data-stu-id="affa7-111">(**MCI\_BREAK** uses the [**MCI\_BREAK\_PARMS**](mci-break-parms.md) structure.) When a wait operation is canceled, MCI attempts to return control to the application without interrupting the command associated with the "wait" flag.</span></span>

 

 

 




