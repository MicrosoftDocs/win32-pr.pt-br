---
description: O procedimento a seguir demonstra como depurar um monitor.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Depurando um monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505849"
---
# <a name="debugging-a-monitor"></a>Depurando um monitor

O procedimento a seguir demonstra como depurar um monitor.

**Para depurar um monitor**

1.  Instale a DLL do monitor e o arquivo do banco de dados do programa (. pdb) gerado quando você compilou o monitor no local correto. Consulte [instalando um monitor para monitor de rede](installing-a-monitor-to-network-monitor.md) para obter mais detalhes.
2.  Verifique se o serviço de controle de monitor está configurado como um servidor, em vez de um serviço, selecionando Painel de controle, serviços.
3.  Abra um prompt de comando e vá para o diretório Monitor de Rede. Tipo:

    **Mcsvc.exe/RegServer**

    Depois que a sessão de depuração do monitor for concluída, você poderá retornar o MCSVC para sua condição padrão digitando:

    **Mcsvc.exe/Service**

4.  Em Microsoft Visual Studio, inicie o Microsoft Visual C++.
5.  Na opção **arquivo**, **abrir** menu, selecione o nome da dll do monitor.
6.  Depois que Microsoft Visual C++ for carregado, clique em **projeto**, **configurações**.
7.  Clique na guia **depurar** em **executável** para sessão de depuração e digite o caminho completo de Mcsvc.exe. Por exemplo, C: \\ Program Files \\ Netmon2 \\Mcsvc.exe.
8.  Defina os pontos de interrupção no código.

> [!Note]  
> Não use uma caixa de mensagem para monitorar a depuração. Se o MCSVC estiver sendo executado como um serviço, você não verá o Popup e o MCSVC parecerá travar.

 

 

 



