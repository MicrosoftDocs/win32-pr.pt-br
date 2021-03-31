---
title: Estruturas-StoServe
description: O copaper empacota a cor, a largura e as coordenadas da caneta em estruturas INKDATA e as armazena em uma matriz alocada dinamicamente que ela gerencia na memória.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916172"
---
# <a name="structures---stoserve"></a>Estruturas-StoServe

O copaper empacota a cor, a largura e as coordenadas da caneta em estruturas **INKDATA** e as armazena em uma matriz alocada dinamicamente que ela gerencia na memória.

## <a name="inkdata-structure"></a>Estrutura INKDATA

A seguir estão as declarações para a estrutura **INKDATA** do paper. H.

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

A matriz dinâmica desses pacotes **INKDATA** é apontada por m \_ paInkData, um membro da classe de implementação [**IPaper**](ipaper-methods.md) . A matriz é criada dentro do método **IPaper:: InitPaper** com uma alocação inicial. Para obter detalhes, consulte o método **InitPaper** e o método de utilitário NextSlot privado da implementação CIMPIPAPER em Paper. H. Os métodos [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) usam NextSlot para obter novos slots na matriz. A matriz é expandida dinamicamente pelo NextSlot à medida que surge a necessidade.

O cliente chama o método [**IPaper:: Erase**](ipaper-methods.md) para apagar o desenho atual. Esse método não realoca a matriz; Ele simplesmente marca todos os dados de tinta atuais como INKTYPE \_ None e redefine o índice de fim de dados da matriz como zero.

O cliente chama os métodos [**IPaper:: Lock**](ipaper-methods.md) e **Unlock** para gerenciar a propriedade de copapel para desenho. Esses métodos são fornecidos para organizar o acesso entre vários clientes no desenho mantido em um copapel compartilhado.

## <a name="paper_properties-structure"></a>Estrutura de propriedades do papel \_

O cliente chama o método [**IPaper:: Resize**](ipaper-methods.md) para informar ao copaper que o usuário redimensionou o retângulo do papel de desenho atual. Esses dados de coordenadas são mantidos em uma estrutura de **\_ Propriedades de papel** , que é armazenada com os dados de tinta quando todos os dados de papel são armazenados em um arquivo composto.

A seguir está a declaração de **\_ Propriedades de papel** do paper. H.

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

A estrutura de **\_ Propriedades de papel** foi projetada para que novos formatos de dados de tinta possam ser adicionados a qualquer momento, à medida que o componente DllPaper evoluir. A interface [**IPaper**](ipaper-methods.md) é geral o suficiente para que uma versão subsequente do componente DllPaper possa armazenar um formato de dados de tinta diferente ao implementar a mesma interface **IPaper** . Como os métodos de **IPaper** não dependem de um formato de dados de tinta específico, uma nova versão do componente DllPaper que dá suporte a um formato de dados de tinta diferente pode usar essa mesma interface.

As propriedades de papel armazenadas em um arquivo composto registram o tamanho atual da matriz de dados de tinta. O tamanho de matriz adequado pode ser alocado para acomodar os dados de tinta lidos do arquivo.

A estrutura de **\_ Propriedades de papel** também armazena a cor da janela de plano de fundo e o tamanho do retângulo de desenho da superfície de papel.

Embora não seja usado nos exemplos de **StoServe** / **StoClien** , um título de desenho e um nome de autor também podem ser armazenados.

A data de criação e as datas da última modificação não são incluídas nessas propriedades de papel, pois a interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) usada para acessar arquivos compostos gerencia essas informações.

 

 




