---
title: Compilando o exemplo de Project
description: Compilando o exemplo de Project
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player online, compilando projetos de exemplo
- lojas online, compilando projetos de exemplo
- tipo 2 lojas online, compilando projetos de exemplo
- Windows Media Player online, projetos de exemplo
- lojas online, projetos de exemplo
- tipo 2 lojas online, projetos de exemplo
- Windows Media Player online, assistente de projeto
- lojas online, assistente de projeto
- type 2 online stores,project wizard
- plug-ins, assistente de projeto
- Windows Media Player plug-ins, assistente de projeto
- compilando projetos de exemplo
- samples,type 2 online stores
- assistente de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b2f5a4b6d29b227b08654cfcde2a89cc97b224fc756251ae9554f029f22416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763936"
---
# <a name="compiling-the-sample-project"></a>Compilando o exemplo de Project

O assistente gera todos os arquivos necessários para compilar o projeto de exemplo, portanto, você não precisa alterar as configurações padrão do projeto. No Visual Studio, no menu **Build,** clique em **Criar** Solução para criar e registrar o componente COM. Por padrão, a configuração de Depuração está ativa.

> [!Note]  
> No Windows Vista e posterior, o projeto não será construído com êxito, a menos que você execute Visual Studio com um token de acesso de administrador completo. Clique com o botão direito do Visual Studio ícone ou nome e clique **em Executar como administrador.**

 

Antes de tentar criar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas Include e Lib, em que você instalou o SDK do Windows. O compilador e o linker precisarão de acesso a alguns dos arquivos nessas pastas.

Se você tiver Visual Studio utilitário de registro do Visual Studio que vem com o SDK do Windows Vista, seu ambiente de desenvolvimento provavelmente já foi configurado para apontar para as pastas de Inclusão e Lib do SDK do Windows. Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.

Para configurar manualmente Visual Studio, use as etapas a seguir.

1.  No menu **Ferramentas** , clique em **Opções**.
2.  Clique **em Projetos e Soluções** e clique VC++ **Diretórios**.
3.  Em **Mostrar diretórios para**, clique em Incluir arquivos **ou** Arquivos **de biblioteca**.
4.  Adicione os diretórios para os arquivos necessários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando o plug-in para uma loja online do tipo 2](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




