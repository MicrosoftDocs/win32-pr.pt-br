---
title: Autenticação de segurança do servidor RAS
description: quando um servidor RAS Windows NT/Windows 2000 recebe uma chamada, ele invoca a função RasSecurityDialogBegin da DLL de segurança de RAS registrada, se houver uma.
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532bda51d6e9ee0ea90c900fa974827e1840e7e633caf48fbadec5fe6a701a22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028735"
---
# <a name="ras-server-security-authentication"></a>Autenticação de segurança do servidor RAS

quando um servidor RAS Windows NT/Windows 2000 recebe uma chamada, ele invoca a função [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) da DLL de segurança de RAS registrada, se houver uma. Essa chamada notifica a DLL de segurança para iniciar sua autenticação do usuário remoto. O servidor RAS chama **RasSecurityDialogBegin** antes de executar sua autenticação de PPP ou RAS.

A chamada [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) passa as seguintes informações para a DLL de segurança:

-   Um identificador de porta para identificar a conexão.
-   Ponteiros para os buffers a serem usados ao se comunicar com o usuário remoto.
-   Um ponteiro para uma função [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) a ser chamada quando a autenticação for concluída.

O identificador de porta e os ponteiros de buffer são válidos até que a DLL de segurança chame [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) para encerrar a transação de autenticação.

O [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifica o servidor RAS dos resultados da autenticação da DLL de segurança do usuário remoto. Se a DLL de segurança relatar êxito, o servidor RAS continuará com sua autenticação de PPP e RAS do usuário remoto. Se a DLL de segurança informar que o usuário remoto falhou na autenticação ou que ocorreu um erro, o servidor RAS desliga e registra o erro ou a autenticação com falha no log de eventos.

 

 




