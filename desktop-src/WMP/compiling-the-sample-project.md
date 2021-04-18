---
title: Compilando o projeto de exemplo
description: Compilando o projeto de exemplo
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Lojas online do Windows Media Player, compilando projetos de exemplo
- lojas online, compilando projetos de exemplo
- Digite 2 lojas online, compilando projetos de exemplo
- Lojas online do Windows Media Player, projetos de exemplo
- lojas online, projetos de exemplo
- Digite 2 lojas online, projetos de exemplo
- Lojas online do Windows Media Player, assistente de projeto
- lojas online, assistente de projeto
- tipo 2 lojas online, assistente de projeto
- plug-ins, assistente de projeto
- Plug-ins do Windows Media Player, assistente de projeto
- compilando projetos de exemplo
- exemplos, tipo 2 lojas online
- Assistente de projeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770514"
---
# <a name="compiling-the-sample-project"></a>Compilando o projeto de exemplo

O assistente gera todos os arquivos necessários para compilar o projeto de exemplo, para que você não precise alterar as configurações de projeto padrão. No Visual Studio, no menu **Compilar** , clique em **Compilar solução** para compilar e registrar o componente com. Por padrão, a configuração de depuração está ativa.

> [!Note]  
> No Windows Vista e posterior, o projeto não será compilado com êxito, a menos que você execute o Visual Studio com um token de acesso de administrador completo. Clique com o botão direito do mouse no nome ou ícone do Visual Studio e clique em **Executar como administrador**.

 

Antes de tentar compilar o projeto, certifique-se de configurar seu ambiente de desenvolvimento para apontar para as pastas denominadas include e lib em que você instalou o SDK do Windows. O compilador e o vinculador precisarão de acesso a alguns dos arquivos nessas pastas.

Se você executou o utilitário de registro do Visual Studio que acompanha o SDK do Windows Vista, seu ambiente de desenvolvimento provavelmente já foi configurado para apontar para as pastas de SDK do Windows incluir e lib. Caso contrário, você deve configurar manualmente seu ambiente de desenvolvimento.

Para configurar manualmente o Visual Studio, use as etapas a seguir.

1.  No menu **Ferramentas** , clique em **Opções**.
2.  Clique em **projetos e soluções** e, em seguida, clique em **diretórios do vc + +**.
3.  Em **Mostrar diretórios para**, clique em **incluir arquivos** ou **arquivos de biblioteca**.
4.  Adicione os diretórios para os arquivos necessários.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando o plug-in para uma loja online tipo 2](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




