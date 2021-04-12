---
title: Operações de rede do Windows
description: Um aplicativo pode usar as funções WNet para procurar, adicionar ou cancelar conexões de rede em qualquer lugar na hierarquia de rede.
ms.assetid: 8f17af6c-e1b2-4b53-b3f0-698d42beb704
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30326d9ad1299e577c65586cff3df3010c086f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294171"
---
# <a name="windows-networking-operations"></a>Operações de rede do Windows

Um aplicativo pode usar as funções WNet para procurar, adicionar ou cancelar conexões de rede em qualquer lugar na hierarquia de rede.

Uma *conexão persistente* é uma conexão de rede que o sistema restaura automaticamente quando o usuário faz logon. Você pode chamar as funções [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) (ou [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)) e [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a) para controlar se uma conexão de rede é persistente de uma sessão para a próxima.

Para localizar o nome de usuário padrão ou o nome de usuário usado para estabelecer uma conexão de rede, chame a função [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) .

Além de chamar as funções WNet, um processo também pode usar processadores e pipes nomeados para se comunicar com outro processo. Para obter mais informações, consulte [processadores](/windows/desktop/ipc/mailslots) e [pipes](/windows/desktop/ipc/pipes).

 

 