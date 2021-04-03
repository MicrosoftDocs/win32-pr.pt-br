---
title: Passar. CPP
description: No componente do provedor de exemplo, um exemplo de código do analisador de caminho do serviço de diretório está em Parse. cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- ADSI de Parse. cpp
- ADSI do analisador de caminho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ee4df5c1c709fde724385fdf5d5cddbafef338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915891"
---
# <a name="parsecpp"></a>Passar. CPP

No componente do provedor de exemplo, um exemplo de código do analisador de caminho do serviço de diretório está em Parse. cpp. O analisador de caminho é um componente fundamental nos componentes do provedor ADs. Ele verifica a validade sintática de um caminho ADs passado para esse provedor. Se a sintaxe for válida, uma estrutura **ObjectInfo** será construída, que contém uma versão componented do ADspath para esse objeto.

Lembre-se de que essa é apenas uma verificação de sintaxe. Em vez de casos especiais a cada nova iteração do caminho, toda a verificação de caminho deve estar de acordo com as regras de gramática estabelecidas pelo analisador.

A tabela a seguir lista as funções e os métodos implementados em Parse. cpp.



| Item                      | Descrição                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analisa o ADspath passado para ele. Essa função segue as seguintes regras de gramática: <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **SampleDSObject**        | Analisa as seguintes regras de gramática: <SampleDSObject> -> " \\ " " \\ <identifier> \\<Pathname><br/>                                            |
| **ProviderName**          | Adiciona o nome do provedor sintaticamente correto, se não houver.                                                                                                          |
| **PathName**              | Analisa as seguintes regras de gramática: <Pathname>  ->  <Component> " \\ \\ " <Pathname> ou<br/> <Pathname> -> <Component><br/> |
| **Componente**             | Analisa as seguintes regras de gramática: <Identifier> ou<br/> <Identifier> "=" <Identifier><br/>                                              |
| **CLexer::CLexer**        | Construtor padrão.                                                                                                                                                  |
| **CLexer:: ~ CLexer**       | Destruidor padrão.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Gerador de token.                                                                                                                                                             |
| **CLexer::NextChar**      | Recupera o próximo caractere único.                                                                                                                                       |
| **CLexer::P ushBackToken** | Faz backup até o início do último token.                                                                                                                               |
| **CLexer::P ushbackChar**  | Faz backup de um caractere.                                                                                                                                                |
| **CLexer:: ispalavra-chave**     | Verifica a lista de palavras-chave. Definido em Globals. h).                                                                                                                          |
| **AddComponent**          | Adiciona esse componente à matriz de componentes.                                                                                                                            |
| **Addprovidername**       | Adiciona um nome de provedor sintaticamente correto à estrutura **ObjectInfo** .                                                                                            |
| **AddRootRDN**            | Adiciona o nome RDN (nome distinto relativo) da raiz sintaticamente correto à estrutura **ObjectInfo** .                                                            |
| **Tipo de**               | Define o tipo do objeto.                                                                                                                                           |
| **Tipo**                  | Analisa o tipo > grupo "usuário" " \| e assim por diante.                                                                                                                          |



 

 

 





