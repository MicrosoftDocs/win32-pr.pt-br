---
title: Gerenciamento e implantação
description: Os profissionais de ti ou desenvolvedores que se preparando para implantar o Windows 7 terão maior confiança e experimentarão um ciclo de avaliação mais curto devido a melhorias em recursos e ferramentas de geração de imagens.
ms.assetid: 217090c4-6385-4333-a380-f75f2c80e369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105b19ad01cb9208d05e77871be637fdadcb0532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917451"
---
# <a name="management-and-deployment"></a>Gerenciamento e implantação

Os profissionais de ti ou desenvolvedores que se preparando para implantar o Windows 7 terão maior confiança e experimentarão um ciclo de avaliação mais curto devido a melhorias em recursos e ferramentas de geração de imagens. Isso inclui suporte para o gerenciamento de aplicativos, drivers e sistemas operacionais em arquivos de imagem offline. Além disso, a criação e o gerenciamento de imagens serão mais fáceis e estarão disponíveis para uma maior variedade de organizações de ti. Implantar o Windows 7 em computadores de negócios também será mais fácil e rápido, devido às novas ferramentas de migração de ti e tecnologias de implantação automatizadas.

## <a name="windows-powershell-20"></a>Windows PowerShell 2.0

O PowerShell é uma linguagem de script gerenciada Microsoft .NET completa que tem um shell de linha de comando interativo e um ISE (ambiente de script integrado) gráfico. Ele dá suporte à ramificação, loop, funções, depuração, manipulação de exceção e internacionalização. O PowerShell 2,0 faz parte do Windows 7 e oferece vários aprimoramentos e um conjunto crescente de *cmdlets* para diagnósticos do Windows, Microsoft Active Directory, Microsoft serviços de informações da Internet (IIS) e muito mais.

O recurso de comunicação remota do PowerShell 2,0 agora permite que os usuários executem comandos em um ou mais computadores remotos em um único computador que esteja executando o PowerShell. Os desenvolvedores também podem hospedar o PowerShell no IIS para acessar e gerenciar seus servidores.

O PowerShell 2,0 dá suporte ao particionamento e à organização de scripts do PowerShell usando módulos que podem ser distribuídos e implantados como unidades independentes e reutilizáveis. Ele também inclui suporte a transações no mecanismo e APIs do PowerShell, o que significa que os desenvolvedores podem iniciar, confirmar e reverter transações usando *cmdlets* de transação internos. Além disso, o mecanismo do PowerShell inclui suporte a eventos para escuta, encaminhamento e ação sobre gerenciamento e eventos do sistema. Os aplicativos do PowerShell podem ser gravados para assinar determinados eventos para processamento síncrono ou assíncrono. (Consulte [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx).)

![captura de tela do ISE do Windows PowerShell](images/windows7-devguide-solidfig1-powershell.jpg)

Figura 1. O Windows PowerShell é uma linguagem de script gerenciada completa do .NET que tem um shell de linha de comando interativo e um ISE gráfico

## <a name="windows-installer"></a>Windows Installer

O Windows Installer foi atualizado para aumentar a eficiência do desenvolvedor, reduzindo a quantidade de código personalizado que é necessária para criar um pacote de instalação e criar instalações de software reais por usuário.

Várias transações de pacote permitem que os desenvolvedores criem uma única transação de vários pacotes usando um "encadeamento" para incluir dinamicamente os pacotes na transação. Se um ou mais dos pacotes não forem instalados conforme o esperado, basta reverter a instalação.

O manipulador de interface do usuário inserida facilita a integração de UIs personalizadas por meio da inserção de um manipulador de interface de utilizador personalizado no pacote de Windows Installer.

O encadeamento de vários pacotes incorporado permite que os desenvolvedores habilitem eventos de instalação em vários pacote. Por exemplo, eles podem habilitar eventos de instalação sob demanda, eventos de reparo e eventos de desinstalação em vários pacotes.

Os novos recursos também permitem a criação de instalações verdadeiras por usuário, incluindo suporte para arquivos de programas por usuário e a funcionalidade "elevar agora" e fornecem suporte para inventário de software offline e verificações de aplicabilidade de patch por meio do gerenciamento e manutenção de imagens de implantação. (Veja [o que há de novo no Windows Installer 5,0](../msi/what-s-new-in-windows-installer-5-0.md).)

 

 