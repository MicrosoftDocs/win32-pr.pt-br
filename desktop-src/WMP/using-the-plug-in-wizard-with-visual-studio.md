---
title: Usando o assistente de plug-in com o Visual Studio
description: Usando o assistente de plug-in com o Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Plug-ins do Windows Media Player, Visual Studio
- plug-ins, Visual Studio
- Criando plug-ins, Visual Studio
- Assistente de plug-in do Windows Media Player, Visual Studio
- Visual Studio, assistente de plug-in do Windows Media Player
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292367"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a>Usando o assistente de plug-in com o Visual Studio

Depois de instalar os componentes necessários, você poderá criar rapidamente um plug-in que servirá como ponto de partida. As etapas a seguir vão orientá-lo.

1.  Inicie o Microsoft Visual Studio.
2.  No menu **arquivo** , aponte para **novo** e clique em **projeto**.
3.  Em **tipos de projeto**, selecione **projetos de Visual C++**.
4.  Em **modelos**, selecione **Assistente de plug-in do Windows Media Player**.
5.  Insira um nome para seu projeto.
6.  Insira um local para seu projeto. Essa é a pasta para a qual os arquivos de projeto serão copiados.
7.  Clique em **OK** para iniciar o assistente.
8.  Selecione o tipo de plug-in que você deseja criar.
9.  Conclua todas as caixas de diálogo restantes no assistente.
10. Use o ambiente de desenvolvimento do Visual Studio para compilar seu projeto.
    > [!Note]  
    > No Windows Vista e posterior, o projeto não será compilado com êxito, a menos que você execute o Visual Studio com um token de acesso de administrador completo. Clique com o botão direito do mouse no nome ou ícone do Visual Studio e clique em **Executar como administrador**.

     

Antes de tentar compilar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas include e lib em que você instalou o SDK do Windows. O compilador e o vinculador precisarão de acesso a alguns dos arquivos nessas pastas.

Se você executou o utilitário de registro do Visual Studio que acompanha o SDK do Windows, o ambiente de desenvolvimento provavelmente já foi configurado para apontar para o SDK do Windows pastas include e lib. Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.

Para configurar manualmente o Visual Studio, use as etapas a seguir.

1.  No menu **Ferramentas** , clique em **Opções**.
2.  Clique em **projetos e soluções** e, em seguida, clique em **diretórios do vc + +**.
3.  Em **Mostrar diretórios para**, clique em **incluir arquivos** ou **arquivos de biblioteca**.
4.  Adicione os diretórios para os arquivos necessários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um plug-in](building-a-plug-in.md)
</dt> </dl>

 

 




