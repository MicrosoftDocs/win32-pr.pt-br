---
title: Usando o assistente de plug-in da loja online com o Visual Studio
description: Usando o assistente de plug-in da loja online com o Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Repositórios online do Windows Media Player, plug-ins
- lojas online, plug-ins
- Digite 1 lojas online, plug-ins
- Repositórios online do Windows Media Player, assistente de plug-in
- repositórios online, assistente de plug-in
- tipo 1 lojas online, assistente de plug-in
- Lojas online do Windows Media Player, Visual Studio
- lojas online, Visual Studio
- Digite 1 lojas online, Visual Studio
- plug-ins, lojas online do Windows Media Player
- plug-ins, lojas online
- plug-ins, digite 1 lojas online
- plug-ins, Visual Studio
- plug-ins, assistente de plug-in
- Plug-ins do Windows Media Player, tipo 1 lojas online
- Plug-ins do Windows Media Player, lojas online
- Plug-ins do Windows Media Player, lojas online do Windows Media Player
- Plug-ins do Windows Media Player, Visual Studio
- Plug-ins do Windows Media Player, assistente de plug-in
- Visual Studio, assistente de lojas online do Windows Media Player
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105807824"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a>Usando o assistente de plug-in da loja online com o Visual Studio

Depois de instalar os componentes necessários, você poderá criar rapidamente um plug-in que servirá como ponto de partida. As etapas a seguir irão guiá-lo:

1.  Inicie o Microsoft Visual Studio.
2.  No menu **arquivo** , aponte para **novo** e clique em **projeto**.
3.  Em **tipos de projeto**, clique em **Visual C++ projetos**.
4.  Em **modelos**, clique em **Assistente de lojas online do Windows Media Player**.
5.  Insira um nome para seu projeto.
6.  Insira um local para seu projeto. Essa é a pasta para a qual os arquivos de projeto serão copiados.
7.  Clique em **OK** para iniciar o assistente.
8.  Selecione **tipo 1 (integração profunda)** e clique em **Avançar**.
9.  Insira um nome amigável e um distribuidor de conteúdo. Clique em **Concluir**.
10. Use o ambiente de desenvolvimento do Visual Studio para compilar seu projeto.
    > [!Note]  
    > No Windows Vista e posterior, o projeto não será compilado com êxito, a menos que você execute o Visual Studio com um token de acesso de administrador completo. Clique com o botão direito do mouse no nome ou ícone do Visual Studio e clique em **Executar como administrador**.

     

Antes de tentar compilar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas include e lib em que você instalou o SDK do Windows. O compilador e o vinculador precisarão de acesso a alguns dos arquivos nessas pastas.

Se você executou o utilitário de registro do Visual Studio que acompanha o SDK do Windows, o ambiente de desenvolvimento provavelmente já foi configurado para apontar para o SDK do Windows pastas include e lib. Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.

Para configurar manualmente o Visual Studio, use as etapas a seguir.

1.  No menu **ferramentas** , clique em opções.
2.  Clique em **projetos e soluções** e, em seguida, clique em **diretórios do vc + +**.
3.  Em **Mostrar diretórios para**, clique em **incluir arquivos** ou **arquivos de biblioteca**.
4.  Adicione os diretórios para os arquivos necessários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando o plug-in para uma loja online tipo 1](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




