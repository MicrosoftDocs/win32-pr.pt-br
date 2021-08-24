---
description: Windows o instalador é integrado à diretiva de restrição de Software no Microsoft Windows XP.
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Política de restrição de software e instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e96d1c422b38fd82110cac34953f24be39909eeb64fa2236d3a993925a55c6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786556"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Política de restrição de software e instalador

Windows o instalador é integrado à diretiva de restrição de Software no Microsoft Windows XP. A diretiva de restrição de software é configurável por meio da diretiva de grupo. A diretiva de restrição de software permite que um administrador restrinja administradores e não administradores de executar arquivos com base nos critérios de caminho, zona de URL, hash ou Publicador. A política de restrição de software tem dois níveis: irrestrito e não permitido. o Windows Installer instala apenas os pacotes com permissão para serem executados no nível irrestrito.

Patches ou transformações também devem ter permissão para serem executados no nível irrestrito. se um pacote, patch ou transformação estiver configurado para ser executado em um nível diferente de irrestrito, o Windows Installer exibirá uma mensagem de erro e registrará uma entrada no log de eventos do aplicativo. A diretiva de restrição de software é avaliada na primeira vez em que um aplicativo é instalado, quando um novo patch é aplicado e quando o pacote de instalação é armazenado em cache novamente.

se um pacote, patch ou transformação for restrito, o Windows Installer exibirá uma mensagem de erro e gravará uma entrada de [log de eventos](event-logging.md) no log de eventos do aplicativo. A diretiva de restrição de software é avaliada na primeira vez em que um aplicativo é instalado, quando um novo patch é aplicado e quando o pacote de instalação é armazenado em cache novamente.

Para obter mais informações sobre a diretiva de restrição de software, consulte a documentação do produto e [pesquise no site do TechNet](https://www.microsoft.com/technet/sitemap.mspx).

 

 



