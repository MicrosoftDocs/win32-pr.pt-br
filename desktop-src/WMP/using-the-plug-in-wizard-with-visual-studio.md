---
title: Usando o assistente de plug-in com Visual Studio
description: Usando o assistente de plug-in com Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- plug-ins Windows Media Player, Visual Studio
- plug-ins, Visual Studio
- Criando plug-ins, Visual Studio
- Windows Media Player Assistente de plug-in, Visual Studio
- assistente de Plug-in do Visual Studio, Windows Media Player
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534d084d2c57d3546427db59274d1bd135bc66e8bf396906ff7776cae9a370f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134329"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Usando o assistente de plug-in com Visual Studio

Depois de instalar os componentes necessários, você poderá criar rapidamente um plug-in que servirá como ponto de partida. As etapas a seguir vão orientá-lo.

1.  Inicie o Microsoft Visual Studio.
2.  No menu **arquivo** , aponte para **novo** e clique em **Project**.
3.  em **tipos de Project**, selecione **Visual C++ projetos**.
4.  em **modelos**, selecione **Windows Media Player assistente de Plug-in**.
5.  Insira um nome para seu projeto.
6.  Insira um local para seu projeto. Essa é a pasta para a qual os arquivos de projeto serão copiados.
7.  Clique em **OK** para iniciar o assistente.
8.  Selecione o tipo de plug-in que você deseja criar.
9.  Conclua todas as caixas de diálogo restantes no assistente.
10. Use o ambiente de desenvolvimento Visual Studio para compilar seu projeto.
    > [!Note]  
    > no Windows Vista e posterior, o projeto não será compilado com êxito, a menos que você execute Visual Studio com um token de acesso de administrador completo. clique com o botão direito do mouse no nome ou ícone do Visual Studio e clique em **executar como administrador**.

     

antes de tentar compilar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas Include e Lib em que você instalou o SDK do Windows. O compilador e o vinculador precisarão de acesso a alguns dos arquivos nessas pastas.

se você executou o utilitário de registro Visual Studio que vem com o SDK do Windows, seu ambiente de desenvolvimento provavelmente já foi configurado para apontar para as pastas SDK do Windows incluir e Lib. Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.

para configurar manualmente Visual Studio, use as etapas a seguir.

1.  No menu **Ferramentas** , clique em **Opções**.
2.  clique em **projetos e soluções** e, em seguida, clique em **VC++ diretórios**.
3.  Em **Mostrar diretórios para**, clique em **incluir arquivos** ou **arquivos de biblioteca**.
4.  Adicione os diretórios para os arquivos necessários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um plug-in](building-a-plug-in.md)
</dt> </dl>

 

 




