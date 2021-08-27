---
title: Chamando APIs de Acessibilidade Ativa
description: O Microsoft Acessibilidade Ativa fornece APIs (interfaces de programação de aplicativo) para clientes e servidores.
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a54bc297af42546a081c3478ef109be137d8af19a37ea39415e8b0d2c06ccc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122236"
---
# <a name="calling-active-accessibility-apis"></a>Chamando APIs de Acessibilidade Ativa

O Microsoft Acessibilidade Ativa fornece APIs (interfaces de programação de aplicativo) para clientes e servidores. a maioria deles é implementada na biblioteca de vínculo dinâmico do Microsoft Acessibilidade Ativa, Oleacc.dll, mas [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)e [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) são implementadas no user32.dll, que é um componente principal do sistema operacional Microsoft Windows.

os computadores que executam o Windows 95 ou o microsoft Windows NT 4,0 não têm Oleacc.dll e a versão correta do user32.dll instalados porque o Microsoft Acessibilidade Ativa foi incorporado em estágios em versões com êxito do Windows. Como resultado, os aplicativos executados nessas plataformas vinculam-se explicitamente a Oleacc.dll em tempo de execução usando a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) em vez de depender de bibliotecas de importação. o Acessibilidade Ativa 1,3 dá suporte a Windows 95 e Microsoft Windows NT 4,0. as versões anteriores do Windows não são suportadas pelo Microsoft Acessibilidade Ativa.

Os aplicativos de servidor usam a função [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar o endereço de uma função de acessibilidade ativa da Microsoft e, em seguida, fazer a chamada por meio de um ponteiro de função. Se você chamar uma função que foi implementada no Oleacc.dll, os aplicativos de servidor usarão o identificador retornado de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) na chamada para **GetProcAddress**. Se chamar uma função definida no user32.dll, os aplicativos de servidor chamarão [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) ESPECIFICANDO "user32" e usarão o identificador de módulo retornado na chamada para **GetProcAddress**.

Por exemplo, se um aplicativo usar [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), ele chamará [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) usando o identificador de módulo de user32.dll para obter o endereço da função. se a chamada for bem-sucedida (o que significa que essa versão do Windows dá suporte ao Microsoft Acessibilidade Ativa), o aplicativo define um sinalizador que indica que é seguro chamar **NotifyWinEvent**. O endereço recebido de **GetProcAddress** é armazenado em uma variável de ponteiro de função e usado em todo o código.

 

 