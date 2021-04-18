---
description: Há suporte para a substituição de recursos protegidos por meio dos mecanismos a seguir.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Mecanismos de substituição de recursos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796146"
---
# <a name="supported-resource-replacement-mechanisms"></a>Mecanismos de substituição de recursos com suporte

Há suporte para a substituição de recursos protegidos por meio dos mecanismos a seguir.

Permissão para acesso completo para modificar recursos protegidos por WRP no Windows Vista e no Windows Server 2008 é restrita ao TrustedInstaller com o serviço instalador de módulos do Windows usando os seguintes mecanismos:

-   Service Packs do Windows instalados pelo TrustedInstaller.
-   Hotfixes instalados pelo TrustedInstaller.
-   Atualizações do sistema operacional instaladas pelo TrustedInstaller.
-   Windows Update instalado pelo TrustedInstaller.

Os aplicativos e instaladores tentando substituir um recurso protegido por WRP por meio de outros métodos especificados têm acesso negado para alterar o recurso e gerar uma mensagem de erro de acesso negado.

Para instaladores conhecidos que tentam substituir recursos protegidos por WRP, o erro de acesso negado e a mensagem de erro podem ser suprimidos. Nesse caso, a operação retorna com êxito, o erro e a mensagem de erro são suprimidos, mas nenhuma alteração é aplicada ao recurso protegido por WRP. O erro pode ser suprimido para um instalador bem conhecido somente quando todos os critérios a seguir são atendidos:

-   Este é um aplicativo herdado. O aplicativo não inclui um manifesto com um requestedExecutionlevel que identifica o aplicativo como projetado para o Windows Vista ou o Windows Server 2008.
-   O erro de acesso negado é causado apenas pela tentativa de modificar um recurso protegido por WRP.
-   Um administrador está instalando o aplicativo.

Para obter informações sobre como usar o Windows Installer com a WRP, consulte [usando Windows Installer e proteção de recursos do Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) no SDK do [Windows Installer](/windows/desktop/Msi/windows-installer-portal) .

**Windows Server 2003 e Windows XP:** A substituição de arquivos do sistema protegidos por WFP tem suporte apenas por meio dos seguintes mecanismos:

-   Instalação do Service Pack do Windows usando o Update.exe
-   Hotfixes instalados usando o Hotfix.exe
-   Atualizações do sistema operacional usando o Winnt32.exe
-   Windows Update

A substituição de arquivos protegidos por meios diferentes desses métodos especificados resulta na restauração dos arquivos originais pela WFP.

 

 
