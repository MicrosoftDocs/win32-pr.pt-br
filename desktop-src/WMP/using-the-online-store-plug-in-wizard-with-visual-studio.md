---
title: Usando o assistente de plug-in da loja online com Visual Studio
description: Usando o assistente de plug-in da loja online com Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player lojas online, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Windows Media Player repositórios online, assistente de plug-in
- repositórios online, assistente de plug-in
- tipo 1 lojas online, assistente de plug-in
- Windows Media Player lojas online Visual Studio
- lojas online, Visual Studio
- Digite 1 lojas online, Visual Studio
- plug-ins, Windows Media Player lojas online
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, Visual Studio
- plug-ins, assistente de plug-in
- plug-ins Windows Media Player, tipo 1 lojas online
- plug-ins Windows Media Player, lojas online
- Windows Media Player plug-ins, Windows Media Player lojas online
- plug-ins Windows Media Player, Visual Studio
- plug-ins Windows Media Player, assistente de plug-in
- Visual Studio, Windows Media Player assistente de repositórios Online
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd53a1b83f817e4cfcc7dede80361f56f46ea41da8730f4396330c12af05c73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830677"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Usando o assistente de plug-in da loja online com Visual Studio

Depois de instalar os componentes necessários, você poderá criar rapidamente um plug-in que servirá como ponto de partida. As etapas a seguir irão guiá-lo:

1.  Inicie o Microsoft Visual Studio.
2.  No menu **arquivo** , aponte para **novo** e clique em **Project**.
3.  em **tipos de Project**, clique em **projetos de Visual C++**.
4.  em **modelos**, clique em **Windows Media Player assistente de lojas Online**.
5.  Insira um nome para seu projeto.
6.  Insira um local para seu projeto. Essa é a pasta para a qual os arquivos de projeto serão copiados.
7.  Clique em **OK** para iniciar o assistente.
8.  Selecione **tipo 1 (integração profunda)** e clique em **Avançar**.
9.  Insira um nome amigável e um distribuidor de conteúdo. Clique em **Concluir**.
10. Use o ambiente de desenvolvimento Visual Studio para compilar seu projeto.
    > [!Note]  
    > no Windows Vista e posterior, o projeto não será compilado com êxito, a menos que você execute Visual Studio com um token de acesso de administrador completo. clique com o botão direito do mouse no nome ou ícone do Visual Studio e clique em **executar como administrador**.

     

antes de tentar compilar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas Include e Lib em que você instalou o SDK do Windows. O compilador e o vinculador precisarão de acesso a alguns dos arquivos nessas pastas.

se você executou o utilitário de registro Visual Studio que vem com o SDK do Windows, seu ambiente de desenvolvimento provavelmente já foi configurado para apontar para as pastas SDK do Windows incluir e Lib. Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.

para configurar manualmente Visual Studio, use as etapas a seguir.

1.  No menu **ferramentas** , clique em opções.
2.  clique em **projetos e soluções** e, em seguida, clique em **VC++ diretórios**.
3.  Em **Mostrar diretórios para**, clique em **incluir arquivos** ou **arquivos de biblioteca**.
4.  Adicione os diretórios para os arquivos necessários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando o plug-in para uma loja online tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




