---
title: ANALISAR. CPP
description: No componente do provedor de exemplo, um exemplo de código do analisador de caminho de serviço de diretório está em Parse.cpp.
ms.assetid: 5d68065b-0dab-41c9-baf1-f9610656bd6e
ms.tgt_platform: multiple
keywords:
- PARSE.cpp ADSI
- ADSI do analisador de caminho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518db6857f9b7018a0dbf3e1e97ac60ed654447d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880284"
---
# <a name="parsecpp"></a>ANALISAR. CPP

No componente do provedor de exemplo, um exemplo de código do analisador de caminho de serviço de diretório está em Parse.cpp. O analisador de caminho é um componente-chave nos componentes do provedor do ADS. Ele verifica a validade sintática de um caminho do ADs passado para esse provedor. Se a sintaxe for válida, uma **estrutura OBJECTINFO** será construída, que contém uma versão componente do ADspath para este objeto.

Esteja ciente de que essa é apenas uma verificação de sintaxe. Em vez de casos especiais a cada nova iteração de caminho, toda a verificação de caminho deve estar em conformidade com as regras de gramática estabelecidas pelo analisador.

A tabela a seguir lista as funções e métodos implementados em Parse.cpp.



| Item                      | Descrição                                                                                                                                                            |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADsObject**             | Analisado o ADspath passado para ele. Essa função segue as seguintes regras de gramática: &lt; ADsObject &gt;  ->  &lt; ProviderName &gt; &lt; SampleDSObject&gt;<br/>     |
| **SampleDSObject**        | Analisar as seguintes regras de gramática: &lt; SampleDSObject &gt; -> \\ \\ " " &lt; identificador " " " &gt; \\ &lt; Pathname&gt;<br/>                                            |
| **ProviderName**          | Adiciona o nome do provedor sintaticamente correto se não houver.                                                                                                          |
| **PathName**              | Análise das seguintes regras de gramática: &lt; Componente Pathname &gt;  ->  &lt; " " &gt; " \\ \\ &lt; Pathname &gt; OR<br/> &lt;Componente &gt;  ->  &lt; Pathname&gt;<br/> |
| **Componente**             | Analisar as seguintes regras de gramática: &lt; Identificador &gt; OR<br/> &lt;Identificador &gt; "=" &lt; Identificador&gt;<br/>                                              |
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



 

 

 





