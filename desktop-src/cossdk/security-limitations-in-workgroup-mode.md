---
description: Limitações de segurança no modo de grupo de trabalho
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Limitações de segurança no modo de grupo de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabe38b8d05c49382ae6dd8337b883a6f4a8079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760672"
---
# <a name="security-limitations-in-workgroup-mode"></a><span data-ttu-id="fa717-103">Limitações de segurança no modo de grupo de trabalho</span><span class="sxs-lookup"><span data-stu-id="fa717-103">Security Limitations in Workgroup Mode</span></span>

<span data-ttu-id="fa717-104">A configuração do grupo de trabalho do [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) não permite que o serviço de componentes em fila com+ ofereça suporte à segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fa717-104">The [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) workgroup configuration does not permit the COM+ queued components service to support application security.</span></span> <span data-ttu-id="fa717-105">Se você tiver instalado o enfileiramento de mensagens com a configuração de grupo de trabalho, deverá [desabilitar a segurança](specifying-the-authentication-protocol.md) em cada aplicativo em fila acessado nessa configuração selecionando não **autenticar mensagens** na guia **enfileiramento** da caixa de diálogo de **Propriedades** do aplicativo com+, usando a ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="fa717-105">If you've installed Message Queuing with the workgroup configuration, you must [disable security](specifying-the-authentication-protocol.md) on each queued application accessed in this configuration by selecting **Do not authenticate messages** on the **Queuing** tab for the COM+ application's **Properties** dialog, using the Component Services administrative tool.</span></span> <span data-ttu-id="fa717-106">Isso deve ser feito somente em uma rede confiável e deve ser feito no cliente e no servidor se o aplicativo já tiver sido exportado.</span><span class="sxs-lookup"><span data-stu-id="fa717-106">This should be done only on a trusted network and must be done at both client and server if the application has already been exported.</span></span>

 

 



