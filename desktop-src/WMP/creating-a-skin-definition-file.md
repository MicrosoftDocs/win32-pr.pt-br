---
title: Criando um arquivo de definição de capa
description: Criando um arquivo de definição de capa
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Windows Media Player Capas móveis, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, criando
- Criando capas, sobre
- criando capas, Windows Media Player dispositivos móveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bb18289a8ed124c820e983c37ccc9fff60c5c1c2b0794e4964a8e170c84909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341596"
---
# <a name="creating-a-skin-definition-file"></a>Criando um arquivo de definição de capa

Um arquivo de definição de capa é um arquivo de texto que define uma capa e todas as suas partes de composição. A extensão de nome de arquivo deve ser. skn.

Todo arquivo de definição de capa deve começar com a linha a seguir, que especifica o número de versão do arquivo de capa. a tabela a seguir mostra Windows Media Player versões e a linha de código que devem ser usadas para identificar cada uma em um arquivo de definição de capa. Embora alguns dos números nas linhas de código não sejam o que você espera, eles estão corretos, conforme mostrado na tabela a seguir.



| versão do Windows Media Player | Primeira linha do arquivo de definição de capa |
|------------------------------|------------------------------------|
| 1.01.1<br/>            | \[Arquivo de capa do Pocket WMP v 1.0\]      |
| 1.2                          | \[Arquivo de capa do Pocket WMP v 1.2\]      |
| 7.0                          | \[Arquivo de capa do Pocket WMP v 2.0\]      |
| 7.1                          | \[Arquivo de capa do Pocket WMP v 8.0\]      |
| 9 Series                     | \[Arquivo de capa 9.0.1 do Pocket WMP v\]    |
| 10 Mobile                    | \[Arquivo de capa 9.0.1 do Pocket WMP v\]    |
| 10,1 móvel                  | \[Arquivo de capa 9.0.1 do Pocket WMP v\]    |



 

o número de versão 9.0.1 é para capas criadas especificamente para Windows Media Player 9 Series ou posterior. as capas com um número de versão anterior são abertas pelo Windows Media Player 9 Series ou posterior como modo retrato, 96 pontos por polegada (DPI).

O arquivo de definição de capa consiste em várias seções. Cada seção define uma área específica da capa. As seções devem ser colocadas na seguinte ordem:

1.  Descrição
2.  Bitmaps
3.  Vídeo
4.  Botões
5.  Status
6.  Texto
7.  Marquee
8.  Trackbars

Cada seção começa com o nome da seção entre colchetes, por exemplo:


```C++
[ Bitmaps ]

```



> [!Note]  
> O arquivo de definição de capa não será analisado corretamente, a menos que você inclua espaços entre colchetes e o nome da seção.

 

Em seguida, uma ou mais linhas definem imagens individuais, botões e assim por diante. Por exemplo, uma seção bitmaps pode incluir o seguinte:


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



Não é necessário alinhar os valores em colunas, mas isso ajudará o seu código a ser mais legível. Para obter mais detalhes sobre cada seção do arquivo de definição de capa, consulte a [referência de capa](skin-reference.md).

> [!Note]  
> Não use guias em qualquer lugar do arquivo; em vez disso, use espaços extras. Isso é muito importante, pois pressionar a tecla TAB durante a gravação ou edição do arquivo de definição de capa fará com que toda a capa falhe. Cada linha deve ser concluída e não pode continuar em uma segunda linha. além disso, a região e os Super valores são preteridos para capas usadas com o Windows Media Player 10 Mobile ou posterior.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Arquivo de definição de capa**](skin-definition-file-mobile.md)
</dt> </dl>

 

 





