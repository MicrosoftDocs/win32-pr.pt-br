---
title: Analisar. Cpp
description: No componente do provedor de exemplo, um exemplo de código do analisador de caminho de serviço de diretório está em Parse.cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- PARSE.cpp ADSI
- ADSI do analisador de caminho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 544ab295318ac80ed19df39a7e5837b566615903a8d8bb963b6fdd5435efde8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023284"
---
# <a name="parsecpp"></a>Analisar. Cpp

No componente do provedor de exemplo, um exemplo de código do analisador de caminho de serviço de diretório está em Parse.cpp. O analisador de caminho é um componente-chave nos componentes do provedor do ADS. Ele verifica a validade sintática de um caminho do ADs passado para esse provedor. Se a sintaxe for válida, uma **estrutura OBJECTINFO** será construída, que contém uma versão componente do ADspath para este objeto.

Esteja ciente de que essa é apenas uma verificação de sintaxe. Em vez de casos especiais a cada nova iteração de caminho, toda a verificação de caminho deve estar em conformidade com as regras de gramática estabelecidas pelo analisador.

A tabela a seguir lista as funções e métodos implementados em Parse.cpp.



| Item                      | Descrição                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analisado o ADspath passado para ele. Essa função segue as seguintes regras de gramática: <ADsObject>  ->  <ProviderName><SampleDSObject><br/>     |
| **SampleDSObject**        | Analisar as seguintes regras de gramática: <SampleDSObject> -> " \\ \\ " " <identifier> \\ "<Pathname><br/>                                            |
| **ProviderName**          | Adiciona o nome do provedor sintaticamente correto se não houver.                                                                                                          |
| **PathName**              | Analisar as seguintes regras de gramática: <Pathname>  ->  <Component> " \\ \\ " <Pathname> OR<br/> <Pathname> -> <Component><br/> |
| **Componente**             | Analisar as seguintes regras de gramática: <Identifier> OR<br/> <Identifier> "=" <Identifier><br/>                                              |
| **CLexer::CLexer**        | Construtor padrão.                                                                                                                                                  |
| **CLexer::~CLexer**       | Destruidor padrão.                                                                                                                                                   |
| **CLexer::GetNextToken**  | Tokenizer.                                                                                                                                                             |
| **CLexer::NextChar**      | Recupera o próximo caractere único.                                                                                                                                       |
| **CLexer::P backToken** | Fazer o back-up até o início do último token.                                                                                                                               |
| **CLexer::P backChar**  | Fazer o back-up de um caractere.                                                                                                                                                |
| **CLexer::IsKeyword**     | Verifica a lista de palavras-chave. Definido em Globals.h).                                                                                                                          |
| **Addcomponent**          | Adiciona esse componente à matriz de componentes.                                                                                                                            |
| **AddProviderName**       | Adiciona um nome de provedor sintaticamente correto à **estrutura OBJECTINFO.**                                                                                            |
| **AddRootRDN**            | Adiciona o nome diferenciado relativo (RDN) da raiz sintaticamente correto à **estrutura OBJECTINFO.**                                                            |
| **SetType**               | Define o tipo do objeto .                                                                                                                                           |
| **Tipo**                  | Analisar o tipo de > "usuário" \| "grupo" e assim por diante.                                                                                                                          |



 

 

 





