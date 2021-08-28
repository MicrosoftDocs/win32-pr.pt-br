---
description: ICE31 valida todos os estilos de fonte predefinidos usados em controles que exibem texto. Ele também valida que a propriedade DefaultUIFont se refere a um estilo de fonte válido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 783c8b842f80707bbd1ca833fbc7ad1f154a47a0d3aa24377ee58a1c6549bf7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528666"
---
# <a name="ice31"></a>ICE31

ICE31 valida todos os estilos de fonte predefinidos usados em [controles que](controls.md) exibem texto. Ele também valida que a [**propriedade DefaultUIFont**](defaultuifont.md) se refere a um estilo de fonte válido.

Os controles podem ter um estilo de fonte predefinido, conforme descrito em [Adicionando controles e texto.](adding-controls-and-text.md) Para definir o estilo de fonte e fonte de uma cadeia de caracteres de texto, prefixe a cadeia de caracteres exibida com { style} ou \\ {&*style*}. Em que style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhum deles estiver presente, mas a [**propriedade DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada.

ICE31 verifica a coluna Texto [](control-table.md) de cada controle na Tabela de Controle para verificar se existe uma entrada válida na [tabela TextStyle](textstyle-table.md).

ICE31 ignora o [controle ScrollableText](scrollabletext-control.md).

## <a name="results"></a>Resultados

ICE31 posta uma mensagem de erro para estilos indefinido, nomes de estilo muito longos, uma tabela TextStyle ausente e marcas de estilo sem chave de fechamento.

ICE31 posta um aviso se a marca de estilo não estiver no início da linha ou se um controle tiver várias marcas de estilo.

## <a name="example"></a>Exemplo

ICE31 posta os seguintes erros para o exemplo mostrado:

-   O Controle DialogB.Control1 usa TextStyle BadStyle indefinido.
-   O Controle DialogB.Control2 usa TextStyle BadStyle indefinido.
-   O Controle DialogB.Control6 não tem chave de fechamento no estilo de texto.
-   Control DialogB.Control3 especifica um estilo de texto muito longo para ser válido.

O ICE31 posta o seguinte aviso para o exemplo mostrado:

-   A marca de Estilo de Texto em DialogB.Control4 não tem nenhum efeito. Você realmente deseja que ele apareça como texto?

[Tabela de controle](control-table.md) (parcial)



| caixa de diálogo  | Control  | Texto                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DialogA | Control0 | { \\ OKStyle}Este é o texto a ser exibido.                                                                                                                             |
| DialogA | Control1 | {&OKStyle} Este é o texto a ser exibido.                                                                                                                              |
| DialogB | Control1 | {&BadStyle} Este é o texto a ser exibido.                                                                                                                             |
| DialogB | Control2 | { \\ BadStyle}Este é o texto a ser exibido.                                                                                                                            |
| DialogB | Control3 | {&Style que tem mais de 72 caracteres e, portanto, não pode ser um estilo, mesmo que, de alguma forma, você tenha feito isso para obter na tabela TextStyle} Este é o texto a ser exibido. |
| DialogB | Control4 | Aviso { \\ OKStyle}Este é o texto a ser exibido.                                                                                                                     |
| DialogB | Control5 | { \\ OKStyle}{&OKStyle}Este é o texto a ser exibido.                                                                                                                   |
| DialogB | Control6 | { \\ OKStyle Este é o texto a ser exibido.                                                                                                                             |



 

[Tabela TextStyle](textstyle-table.md) (parcial)



| Textstyle |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



