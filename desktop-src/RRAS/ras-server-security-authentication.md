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
# <a name="ras-server-security-authentication"></a>Autenticação de segurança do servidor RAS

Quando um servidor RAS do Windows NT/Windows 2000 recebe uma chamada, ele invoca a função [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) da DLL de segurança RAS registrada, se houver uma. Essa chamada notifica a DLL de segurança para iniciar sua autenticação do usuário remoto. O servidor RAS chama **RasSecurityDialogBegin** antes de executar sua autenticação de PPP ou RAS.

A chamada [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) passa as seguintes informações para a DLL de segurança:

-   Um identificador de porta para identificar a conexão.
-   Ponteiros para os buffers a serem usados ao se comunicar com o usuário remoto.
-   Um ponteiro para uma função [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) a ser chamada quando a autenticação for concluída.

O identificador de porta e os ponteiros de buffer são válidos até que a DLL de segurança chame [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) para encerrar a transação de autenticação.

O [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifica o servidor RAS dos resultados da autenticação da DLL de segurança do usuário remoto. Se a DLL de segurança relatar êxito, o servidor RAS continuará com sua autenticação de PPP e RAS do usuário remoto. Se a DLL de segurança informar que o usuário remoto falhou na autenticação ou que ocorreu um erro, o servidor RAS desliga e registra o erro ou a autenticação com falha no log de eventos.

 

 




