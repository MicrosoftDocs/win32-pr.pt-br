---
description: O AutoRun é um recurso do sistema operacional Windows.
title: Criando um aplicativo de CD-ROM habilitado para AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164321"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Criando um aplicativo de CD-ROM habilitado para AutoRun

O AutoRun é um recurso do sistema operacional Windows. Ele automatiza os procedimentos para instalar e configurar produtos projetados para plataformas baseadas no Windows que são distribuídas em CD-ROMs. Quando os usuários inserem um CD habilitado para AutoRun em sua unidade de CD-ROM, o AutoRun executa automaticamente um aplicativo no CD-ROM que instala, configura ou executa o produto selecionado.

O AutoRun pode ser usado para instalar e executar aplicativos de CD-ROM. Embora o AutoRun seja mais comumente usado para aplicativos do Windows, ele também pode ser usado para instalar, configurar ou executar aplicativos baseados em MS-dos em uma sessão do Windows Microsoft MS-DOS. Você pode configurar cada aplicativo baseado em MS-dos com seu próprio ícone exclusivo, Config.sys arquivo e Autoexec.bat arquivo. O Windows cria os arquivos de configuração corretos para o aplicativo baseado em MS-dos. O aplicativo de inicialização inicia o aplicativo baseado em MS-dos em uma janela.

> [!Note]  
> Para que o AutoRun funcione, a unidade de CD-ROM deve ter drivers de dispositivo 32 ou 64 bits que detectam quando um usuário insere um CD e notifica o sistema.

 

As seções a seguir discutem como implementar um aplicativo de CD-ROM habilitado para AutoRun.

-   [Criando um aplicativo AutoRun-Enabled](autoplay-works.md)
-   [Entradas autorun. inf](autorun-cmds.md)
-   [Habilitando e desabilitando o AutoRun](autoplay-reg.md)

 

 



