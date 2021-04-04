---
title: Usando matrizes, cadeias de caracteres e ponteiros
description: O programa de doutor ( \\ consulte \\ exemplos \\ de RPC Doctor na plataforma SDK (Software Development Kit)) é um bom exemplo de um aplicativo que demonstra as compensações de design envolvidas com os atributos de matriz e cadeia de caracteres.
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542a174b9ffd742ecf88de7231449a780be8dca9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084605"
---
# <a name="using-arrays-strings-and-pointers"></a>Usando matrizes, cadeias de caracteres e ponteiros

O programa de doutor ( \\ consulte \\ exemplos \\ de RPC Doctor na plataforma SDK (Software Development Kit)) é um bom exemplo de um aplicativo que demonstra as compensações de design envolvidas com os atributos de matriz e cadeia de caracteres. O programa de doutor é uma pequena versão de exemplo de um programa mais conhecido, Eliza, desenvolvido pelo pesquisador de inteligência artificial Joseph Weizenbaum no MIT nos anos 60. O programa imita um Therapist usando a correspondência de padrão simples para responder à entrada de idioma natural.

O programa Eliza gravou a sessão a seguir.



| Usuário                                                | Eliza                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| Os homens são todos semelhantes.                                  | De que maneira?                                              |
| Eles estão sempre contratando-nos sobre algo ou outro. | Você pode considerar um exemplo específico?                      |
| Bem, meu namorado me fez aqui.               | Seu namorado fez aqui.                        |
| Ele diz que estou premiado muito do tempo.             | Desculpe-nos ouvir que você está pressionado.                |
| É verdade, sou infeliz.                            | Vocês acham que chegar aqui ajudarão você a não ser infeliz? |
| Preciso de ajuda; Isso parece muito certo.          | O que significa se você tem alguma ajuda?           |
| Talvez eu aprenda a conhecer minha mãe.  | Mais informações sobre sua família.                           |
| Minha mãe cuida de mim.                         | Quem mais em sua família cuida de você?                |
| Meu pai.                                          | Seu pai.                                              |
| Você é como meu pai de algumas maneiras.                | Que aparência você vê?                              |



 

O programa médico pode ser dividido em aplicativos do lado do cliente e do servidor. O lado do cliente solicita a entrada do paciente e exibe a resposta do médico. O lado do servidor processa a entrada do paciente e gera a resposta do médico. Este é um exemplo clássico de um aplicativo cliente-servidor: o cliente é responsável pela interação do usuário, enquanto o servidor manipula a carga computacional extensiva. Muitos dados são passados para e retornados pela função, mas, como os dados podem exigir uma quantidade significativa de processamento, o servidor o processa.

O programa de doutor usa uma matriz de caracteres para entrada e retorna outra matriz de caracteres como saída. A tabela a seguir lista quatro maneiras de passar matrizes de caracteres entre o cliente e o servidor e os atributos e funções necessários para implementar cada abordagem.



| Abordagem                       | Atributos ou funções                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Matrizes de caracteres contadas       | \[[tamanho \_ ](/windows/desktop/Midl/size-is) \] , \[ [comprimento, \_ ](/windows/desktop/Midl/length-is) \] \[ [ref](/windows/desktop/Midl/ref)\]                                         |
| Cadeias de caracteres gerenciadas por stub           | \[[String](/windows/desktop/Midl/string) \] , \[ [ref](/windows/desktop/Midl/ref) \] , [MIDL \_ usuário \_ ALLOCATE](/windows/desktop/Midl/midl-user-allocate-1) no servidor                  |
| Cadeias de caracteres gerenciadas por stub           | \[[cadeia de caracteres](/windows/desktop/Midl/string) \] , \[ [exclusivo](/windows/desktop/Midl/unique) \] , [ \_ \_ alocação de usuário de MIDL](/windows/desktop/Midl/midl-user-allocate-1) no cliente e no servidor |
| Função que retorna uma cadeia de caracteres | \[[exclusivo](/windows/desktop/Midl/unique)\]                                                                                                     |



 

Dentro das restrições associadas a essas combinações de atributos, há maneiras alternativas de enviar uma matriz de caracteres do cliente para o servidor e retornar outra matriz de caracteres do servidor para o cliente.

Os tópicos a seguir demonstram as compensações de design entre as várias interfaces que podem gerenciar esses parâmetros.

-   [Matrizes de caracteres contadas](counted-character-arrays.md)
-   [Cadeias de caracteres](strings.md)
-   [Vários níveis de ponteiros](multiple-levels-of-pointers.md)

 

 