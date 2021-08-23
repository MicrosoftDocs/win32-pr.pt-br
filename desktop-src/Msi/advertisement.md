---
description: O Windows instalador pode anunciar a disponibilidade de um aplicativo para usuários ou outros aplicativos sem realmente instalar o aplicativo.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Anúncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71f9d60eb1d709f0b956719593e2d7158ba8ef2bc17994945302474a02b695a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066366"
---
# <a name="advertisement"></a>Anúncio

O Windows instalador pode anunciar a disponibilidade de um aplicativo para usuários ou outros aplicativos sem realmente instalar o aplicativo. Se um aplicativo for anunciado, somente as interfaces necessárias para carregar e iniciar o aplicativo serão apresentadas ao usuário ou a outros aplicativos. Se um usuário ou aplicativo ativar uma interface anunciada, o instalador prosseguirá para instalar os componentes necessários, conforme descrito em [Instalação sob demanda.](installation-on-demand.md)

Os dois tipos de publicidade estão atribuindo e publicando. Um aplicativo aparece instalado para um usuário quando esse aplicativo é atribuído ao usuário. O  menu Iniciar contém os atalhos apropriados, os ícones são exibidos, os arquivos são associados ao aplicativo e as entradas do Registro refletem a instalação do aplicativo. Quando o usuário tenta abrir um aplicativo atribuído, ele é instalado sob demanda.

O instalador dá suporte ao anúncio de aplicativos e recursos de acordo com o sistema operacional. O instalador registra informações de classe COM para aplicativos atribuídos a partir do Windows XP. Isso permite que o instalador instale o aplicativo após a criação de uma instância de uma classe anunciada. Para obter mais informações, consulte [Suporte à plataforma de anúncio.](platform-support-of-advertisement.md)

Você pode publicar um aplicativo do servidor a partir do Windows Server 2003. O aplicativo publicado é instalado por meio de sua associação de arquivo ou do tipo MIME (Multipurpose Internet Mail Extension). A publicação não preenche a interface do usuário com nenhum dos ícones do aplicativo. O sistema operacional cliente pode instalar um aplicativo publicado a partir do Windows XP.

 

 



