---
title: Requisitos do IIS para carregamentos do BITS
description: Para carregamentos, o BITS requer o IIS 6,0 no Windows Server 2003 e o IIS 7,0 no Windows Server 2008; O BITS não oferece suporte ao IIS 5,1 no Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635108"
---
# <a name="iis-requirements-for-bits-uploads"></a>Requisitos do IIS para carregamentos do BITS

Para carregamentos, o BITS requer o IIS 6,0 no Windows Server 2003 e o IIS 7,0 no Windows Server 2008; O BITS não oferece suporte ao IIS 5,1 no Windows XP. O diretório virtual do IIS deve ser habilitado para carregamentos e ter as extensões do IIS do BITS configuradas.

**Principais instalações do Windows Server:** Não há suporte para extensões do IIS do BITS.

No Windows Server 2008, use o **Gerenciador do servidor** para instalar o recurso de extensões de servidor bits. Em **Gerenciador do servidor**, clique em **recursos** no painel esquerdo. No **Assistente para adicionar recursos**, marque extensões de servidor bits. Observe que as funções de compatibilidade de gerenciamento do IIS 6 devem ser instaladas.

No Windows Server 2003, use o **Assistente de componentes do Windows** para instalar a extensão do servidor bits. No **painel de controle**, selecione **Adicionar ou remover programas**. Em seguida, selecione **Adicionar/remover componentes do Windows** para exibir o **Assistente de componentes do Windows**. A extensão do servidor BITS é um subcomponente do Serviços de Informações da Internet (IIS), que é um subcomponente do servidor de aplicativos da Web.

> [!Note]  
> Se o serviço IISAdmin for reiniciado, o processo de trabalho do IIS deverá ser reciclado antes que o serviço BITS possa retomar os carregamentos. O processo de trabalho do IIS pode ser reciclado manualmente usando o utilitário de linha de comando **IISReset.exe** .

 

Para obter informações sobre como configurar o IIS para carregamentos, consulte [Configurando o servidor para carregamentos](setting-up-the-server-for-uploads.md).

Para obter detalhes sobre as propriedades que o BITS adiciona ao IIS, consulte [configurações do servidor bits para trabalhos de carregamento](bits-server-settings-for-upload-jobs.md).

 

 




