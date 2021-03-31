---
title: Autenticação de segurança do servidor RAS
description: Quando um servidor RAS do Windows NT/Windows 2000 recebe uma chamada, ele invoca a função RasSecurityDialogBegin da DLL de segurança RAS registrada, se houver uma.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005426"
---
# <a name="ras-server-security-authentication"></a><span data-ttu-id="762f6-103">Autenticação de segurança do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="762f6-103">RAS Server Security Authentication</span></span>

<span data-ttu-id="762f6-104">Quando um servidor RAS do Windows NT/Windows 2000 recebe uma chamada, ele invoca a função [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) da DLL de segurança RAS registrada, se houver uma.</span><span class="sxs-lookup"><span data-stu-id="762f6-104">When a Windows NT/Windows 2000 RAS server receives a call, it invokes the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) function of the registered RAS security DLL, if there is one.</span></span> <span data-ttu-id="762f6-105">Essa chamada notifica a DLL de segurança para iniciar sua autenticação do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="762f6-105">This call notifies the security DLL to begin its authentication of the remote user.</span></span> <span data-ttu-id="762f6-106">O servidor RAS chama **RasSecurityDialogBegin** antes de executar sua autenticação de PPP ou RAS.</span><span class="sxs-lookup"><span data-stu-id="762f6-106">The RAS server calls **RasSecurityDialogBegin** before performing its PPP or RAS authentication.</span></span>

<span data-ttu-id="762f6-107">A chamada [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) passa as seguintes informações para a DLL de segurança:</span><span class="sxs-lookup"><span data-stu-id="762f6-107">The [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) call passes the following information to the security DLL:</span></span>

-   <span data-ttu-id="762f6-108">Um identificador de porta para identificar a conexão.</span><span class="sxs-lookup"><span data-stu-id="762f6-108">A port handle to identify the connection.</span></span>
-   <span data-ttu-id="762f6-109">Ponteiros para os buffers a serem usados ao se comunicar com o usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="762f6-109">Pointers to buffers to use when communicating with the remote user.</span></span>
-   <span data-ttu-id="762f6-110">Um ponteiro para uma função [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) a ser chamada quando a autenticação for concluída.</span><span class="sxs-lookup"><span data-stu-id="762f6-110">A pointer to a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) function to call when the authentication has been completed.</span></span>

<span data-ttu-id="762f6-111">O identificador de porta e os ponteiros de buffer são válidos até que a DLL de segurança chame [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) para encerrar a transação de autenticação.</span><span class="sxs-lookup"><span data-stu-id="762f6-111">The port handle and buffer pointers are valid until the security DLL calls [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) to terminate the authentication transaction.</span></span>

<span data-ttu-id="762f6-112">O [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifica o servidor RAS dos resultados da autenticação da DLL de segurança do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="762f6-112">The [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifies the RAS server of the results of the security DLL's authentication of the remote user.</span></span> <span data-ttu-id="762f6-113">Se a DLL de segurança relatar êxito, o servidor RAS continuará com sua autenticação de PPP e RAS do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="762f6-113">If the security DLL reports success, the RAS server proceeds with its PPP and RAS authentication of the remote user.</span></span> <span data-ttu-id="762f6-114">Se a DLL de segurança informar que o usuário remoto falhou na autenticação ou que ocorreu um erro, o servidor RAS desliga e registra o erro ou a autenticação com falha no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="762f6-114">If the security DLL reports that the remote user failed the authentication, or that an error occurred, the RAS server hangs up and logs the error or failed authentication in the event log.</span></span>

 

 




