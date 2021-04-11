---
description: ICE31 valida todos os estilos de fonte predefinidos usados em controles que exibem texto. Ele também valida que a propriedade DefaultUIFont se refere a um estilo de fonte válido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170230"
---
# <a name="ice31"></a>ICE31

ICE31 valida todos os estilos de fonte predefinidos usados em [controles](controls.md) que exibem texto. Ele também valida que a propriedade [**DefaultUIFont**](defaultuifont.md) se refere a um estilo de fonte válido.

Os controles podem ter um estilo de fonte predefinido, conforme descrito em [adicionando controles e texto](adding-controls-and-text.md). Para definir a fonte e o estilo da fonte de uma cadeia de texto, Prefixe a cadeia de caracteres exibidos com { \\ Style} ou {&*Style*}. Em que Style é um identificador listado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). Se nenhuma dessas opções estiver presente, mas a propriedade [**DefaultUIFont**](defaultuifont.md) for definida como um estilo de texto válido, essa fonte será usada.

ICE31 verifica a coluna de texto de cada controle na [tabela de controle](control-table.md) para verificar se existe uma entrada válida na [tabela TextStyle](textstyle-table.md).

ICE31 ignora o [controle ScrollableText](scrollabletext-control.md).

## <a name="results"></a>Resultados

ICE31 posta uma mensagem de erro para estilos indefinidos, nomes de estilo que são muito longos, uma tabela de TextStyle ausente e marcas de estilo sem chave de fechamento.

ICE31 lançará um aviso se a marca de estilo não estiver no início da linha ou se um controle tiver várias marcas de estilo.

## <a name="example"></a>Exemplo

ICE31 posta os seguintes erros para o exemplo mostrado:

-   O controle DialogB. Control1 usa o BadStyle TextStyle indefinido.
-   O controle DialogB. Control2 usa BadStyle TextStyle indefinido.
-   O controle DialogB. Control6 não tem chaves de fechamento no estilo de texto.
-   O controle DialogB. Control3 especifica um estilo de texto muito longo para ser válido.

ICE31 posta o seguinte aviso para o exemplo mostrado:

-   A marca de estilo de texto em DialogB. Control4 não tem efeito. Você realmente deseja que ele apareça como texto?

[Tabela de controle](control-table.md) (parcial)



| caixa de diálogo  | Control  | Texto                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Caixa de diálogo | Control0 | { \\ OKStyle} este é o texto a ser exibido.                                                                                                                             |
| Caixa de diálogo | Control1 | {&OKStyle} Este é o texto a ser exibido.                                                                                                                              |
| DialogB | Control1 | {&BadStyle} Este é o texto a ser exibido.                                                                                                                             |
| DialogB | Control2 | { \\ BadStyle} este é o texto a ser exibido.                                                                                                                            |
| DialogB | Control3 | {&estilo que está acima de 72 caracteres e, portanto, não pode ser um estilo mesmo que, de alguma forma, você tenha gerenciado para obtê-lo na tabela TextStyle} Este é o texto a ser exibido. |
| DialogB | Control4 | Aviso { \\ OKStyle} este é o texto a ser exibido.                                                                                                                     |
| DialogB | Control5 | { \\ OKStyle} {&OKStyle} este é o texto a ser exibido.                                                                                                                   |
| DialogB | Control6 | { \\ OKStyle este é o texto a ser exibido.                                                                                                                             |



 

[Tabela TextStyle](textstyle-table.md) (parcial)



| Estilo] |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



