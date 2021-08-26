---
description: Há suporte para a substituição de recursos protegidos por meio dos mecanismos a seguir.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Mecanismos de substituição de recursos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8f839e65ddd07bbde6bb4e089c3235ee6930dec910c07c1c318e666b034afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999246"
---
# <a name="supported-resource-replacement-mechanisms"></a>Mecanismos de substituição de recursos com suporte

Há suporte para a substituição de recursos protegidos por meio dos mecanismos a seguir.

A permissão para acesso completo para modificar recursos protegidos por WRP no Windows Vista e no Windows Server 2008 é restrita ao TrustedInstaller com o serviço instalador de módulos do Windows usando os seguintes mecanismos:

-   Windows Service Packs instalados pelo TrustedInstaller.
-   Hotfixes instalados pelo TrustedInstaller.
-   Atualizações do sistema operacional instaladas pelo TrustedInstaller.
-   Windows Atualização instalada pelo TrustedInstaller.

Aplicativos e instaladores que tentam substituir um recurso protegido por WRP por meios diferentes desses métodos especificados têm acesso negado para alterar o recurso e gerar uma mensagem de erro de acesso negado.

Para instaladores conhecidos que tentam substituir recursos protegidos por WRP, o erro de acesso negado e a mensagem de erro podem ser suprimidos. Nesse caso, a operação retorna com êxito, o erro e a mensagem de erro são suprimidos, mas nenhuma alteração é aplicada ao recurso protegido por WRP. O erro pode ser suprimido para um instalador conhecido somente quando todos os critérios a seguir são atendidos:

-   Esse é um aplicativo herdado. O aplicativo não inclui um manifesto com um requestedExecutionlevel que identifica o aplicativo como projetado para Windows Vista ou Windows Server 2008.
-   O erro de acesso negado é causado apenas pela tentativa de modificar um recurso protegido por WRP.
-   Um Administrador está instalando o aplicativo.

Para obter informações sobre como usar o Windows com WRP, consulte [Using Windows Installer](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) and Windows Resource Protection no SDK do [Windows Installer.](/windows/desktop/Msi/windows-installer-portal)

**Windows Server 2003 e Windows XP:** Há suporte para a substituição de arquivos do sistema protegidos por WFP apenas por meio dos seguintes mecanismos:

-   Windows Instalação do Service Pack usando Update.exe
-   Hotfixes instalados usando Hotfix.exe
-   Atualizações do sistema operacional usando Winnt32.exe
-   Windows Update

Substituir arquivos protegidos por meios diferentes desses métodos especificados resulta na restauração dos arquivos originais pelo WFP.

 

 
