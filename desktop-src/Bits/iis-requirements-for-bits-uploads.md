---
title: Requisitos do IIS para carregamentos do BITS
description: para carregamentos, o BITS requer o iis 6,0 no Windows server 2003 e o iis 7,0 no Windows server 2008; o BITS não oferece suporte ao IIS 5,1 no Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb09ec8c55cce592baf48b4b39faf031e5d6c98909927c0e597be6aaae8712e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004986"
---
# <a name="iis-requirements-for-bits-uploads"></a>Requisitos do IIS para carregamentos do BITS

para carregamentos, o BITS requer o iis 6,0 no Windows server 2003 e o iis 7,0 no Windows server 2008; o BITS não oferece suporte ao IIS 5,1 no Windows XP. O diretório virtual do IIS deve ser habilitado para carregamentos e ter as extensões do IIS do BITS configuradas.

**principais instalações do Windows Server:** Não há suporte para extensões do IIS do BITS.

no Windows Server 2008, use o **Gerenciador do Servidor** para instalar o recurso extensões de servidor BITS. Em **Gerenciador do servidor**, clique em **recursos** no painel esquerdo. No **Assistente para adicionar recursos**, marque extensões de servidor bits. Observe que as funções de compatibilidade de gerenciamento do IIS 6 devem ser instaladas.

no Windows Server 2003, use o **assistente de componentes do Windows** para instalar a extensão do servidor BITS. No **painel de controle**, selecione **Adicionar ou remover programas**. em seguida, selecione **adicionar/remover Windows componentes** para exibir o **assistente de componentes do Windows**. a extensão do servidor BITS é um subcomponente do Serviços de Informações da Internet (IIS), que é um subcomponente do servidor de aplicativos da Web.

> [!Note]  
> Se o serviço IISAdmin for reiniciado, o processo de trabalho do IIS deverá ser reciclado antes que o serviço BITS possa retomar os carregamentos. O processo de trabalho do IIS pode ser reciclado manualmente usando o utilitário de linha de comando **IISReset.exe** .

 

Para obter informações sobre como configurar o IIS para carregamentos, consulte [Configurando o servidor para carregamentos](setting-up-the-server-for-uploads.md).

para obter detalhes sobre as propriedades que o BITS adiciona ao IIS, consulte [Configurações do servidor BITS para trabalhos Upload](bits-server-settings-for-upload-jobs.md).

 

 




