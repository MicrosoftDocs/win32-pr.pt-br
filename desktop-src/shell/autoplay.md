---
description: o AutoRun é um recurso do sistema operacional Windows.
title: Criando um aplicativo de CD-ROM habilitado para AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b8bc1edad7fe49b996dd8471ae8ce081c36c71b7b7df48ca6296b07f8646ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460926"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Criando um aplicativo de CD-ROM habilitado para AutoRun

o AutoRun é um recurso do sistema operacional Windows. ele automatiza os procedimentos para instalar e configurar produtos projetados para plataformas baseadas em Windows que são distribuídas em CD-ROMs. Quando os usuários inserem um CD habilitado para AutoRun em sua unidade de CD-ROM, o AutoRun executa automaticamente um aplicativo no CD-ROM que instala, configura ou executa o produto selecionado.

O AutoRun pode ser usado para instalar e executar aplicativos de CD-ROM. embora o AutoRun seja mais comumente usado para aplicativos Windows, ele também pode ser usado para instalar, configurar ou executar aplicativos baseados em ms-dos em uma sessão Windows Microsoft MS-DOS. Você pode configurar cada aplicativo baseado em MS-dos com seu próprio ícone exclusivo, Config.sys arquivo e Autoexec.bat arquivo. Windows cria os arquivos de configuração corretos para o aplicativo baseado em ms-dos. O aplicativo de inicialização inicia o aplicativo baseado em MS-dos em uma janela.

> [!Note]  
> Para que o AutoRun funcione, a unidade de CD-ROM deve ter drivers de dispositivo 32 ou 64 bits que detectam quando um usuário insere um CD e notifica o sistema.

 

As seções a seguir discutem como implementar um aplicativo de CD-ROM habilitado para AutoRun.

-   [Criando um aplicativo AutoRun-Enabled](autoplay-works.md)
-   [Entradas autorun. inf](autorun-cmds.md)
-   [Habilitando e desabilitando o AutoRun](autoplay-reg.md)

 

 



