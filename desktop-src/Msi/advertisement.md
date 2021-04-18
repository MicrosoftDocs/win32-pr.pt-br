---
description: O Windows Installer pode anunciar a disponibilidade de um aplicativo para usuários ou outros aplicativos sem realmente instalar o aplicativo.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Anúncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749596"
---
# <a name="advertisement"></a>Anúncio

O Windows Installer pode anunciar a disponibilidade de um aplicativo para usuários ou outros aplicativos sem realmente instalar o aplicativo. Se um aplicativo for anunciado, somente as interfaces necessárias para carregar e iniciar o aplicativo serão apresentadas ao usuário ou a outros aplicativos. Se um usuário ou aplicativo ativar uma interface anunciada, o instalador continuará instalando os componentes necessários, conforme descrito em [instalação sob demanda](installation-on-demand.md).

Os dois tipos de publicidade são atribuição e publicação. Um aplicativo aparece instalado para um usuário quando esse aplicativo é atribuído ao usuário. O menu **Iniciar** contém os atalhos apropriados, os ícones são exibidos, os arquivos são associados ao aplicativo e as entradas do registro refletem a instalação do aplicativo. Quando o usuário tenta abrir um aplicativo atribuído, ele é instalado sob demanda.

O instalador oferece suporte ao anúncio de aplicativos e recursos de acordo com o sistema operacional. O instalador registra informações de classe COM para aplicativos atribuídos a partir do Windows XP. Isso permite que o instalador instale o aplicativo na criação de uma instância de uma classe anunciada. Para obter mais informações, consulte [suporte de plataforma do anúncio](platform-support-of-advertisement.md).

Você pode publicar um aplicativo do servidor a partir do Windows Server 2003. O aplicativo publicado é instalado por meio de sua associação de arquivo ou do tipo MIME (Multipurpose Internet Mail Extension). A publicação não preenche a interface do usuário com nenhum dos ícones do aplicativo. O sistema operacional do cliente pode instalar um aplicativo publicado a partir do Windows XP.

 

 



