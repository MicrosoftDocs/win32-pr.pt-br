---
title: Windows Defender Funções
description: Funções chamadas por aplicativos para solicitar verificações, atualizações de assinatura ou informações de Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ecfa00a38c2263fe1db1b996bb3ec052f8caef1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483122"
---
# <a name="windows-defender-functions"></a>Windows Defender Funções

Funções chamadas por aplicativos para solicitar verificações, atualizações de assinatura ou informações de Windows Defender.




| Função | Descrição | 
|----------|-------------|
| <a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a> | Retorna uma mensagem de erro formatada com base em um código de erro.<br /> | 
| <a href="mpfreememory.md"><strong>MpFreeMemory</strong></a> | Libera memória para o gerenciador de proteção contra malware.<br /> | 
| <a href="mphandleclose.md"><strong>MpHandleClose</strong></a> | Fecha o handle retornado por <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>ou <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br /> | 
| <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a> | Estabelece uma conexão com o gerenciador de proteção contra malware no computador local.<br /> | 
| <a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a> | <strong>Sem suporte.</strong> Retorna informações de status sobre vários componentes do gerenciador de proteção contra malware.<br /> | 
| <a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a> | Retorna informações de status sobre vários componentes do gerenciador de proteção contra malware.<br /> | 
| <a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a> | Retorna informações de versão sobre vários componentes do gerenciador de proteção contra malware.<br /> | 
| <a href="mpscancontrol.md"><strong>MpScanControl</strong></a> | Permite o controle de uma verificação iniciada de forma assíncrona por meio <a href="mpscanstart.md"><strong>de MpScanStart.</strong></a><br /> | 
| <a href="mpscanstart.md"><strong>MpScanStart</strong></a> | Inicia uma operação de verificação.<br /> | 
| <a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a> | Retorna informações sobre a próxima ameaça na lista de enumeração. Essa função pode ser chamada repetidamente até que a enumeração de todas as ameaças seja concluída.<br /> | 
| <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a> | Retorna um alça de enumeração para a finalidade de recuperar ameaças. Essa função pode ser usada para abrir ameaças detectadas por uma verificação específica, todas as ameaças ativas no sistema, o histórico de ameaças de ameaça ou todas as ameaças presentes no banco de dados de assinatura.<br /> | 
| <a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a> | Usado para consultar informações estáticas (como severidade e categoria) ou localizadas (como descrição e conselhos de categoria) sobre uma ameaça específica.<br /> | 
| <a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a> | Permite o controle de uma operação de atualização de assinatura iniciada de forma assíncrona por meio <a href="mpupdatestart.md"><strong>de MpUpdateStart</strong></a>.<br /> | 
| <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a> | Inicia uma operação de atualização de assinatura.<br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> | Altera Windows Defender status para on ou off.<br /><blockquote>[!Note]<br />A partir Windows 10, versão 1607 e Windows Server 2016, a <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>função WDEnable</strong></a> sempre retorna <strong>E_NOTIMPL</strong>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a> | Retorna o status atual do Windows Defender.<br /> | 




 

 

 





