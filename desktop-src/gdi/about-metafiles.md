---
description: Internamente, um metarquivo é uma matriz de estruturas de comprimento variável chamada registros de metarquivo.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Sobre os metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc573d54f1f89e2dfe06edb8e225516fe8f0946485592d7d6aaea1faa651de85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779456"
---
# <a name="about-metafiles"></a>Sobre os metaarquivos

Internamente, um metarquivo é uma matriz de estruturas de comprimento variável chamada *registros de metarquivo*. Os primeiros registros no metarquivo especificam informações gerais, como a resolução do dispositivo no qual a imagem foi criada, as dimensões da imagem e assim por diante. Os registros restantes, que constituem a massa de qualquer metarquivo, correspondem às funções da interface de dispositivo de gráficos (GDI) necessárias para desenhar a imagem. Esses registros são armazenados no metarquivo após a criação de um contexto de dispositivo de metarquivo especial. Esse contexto de dispositivo de metarquivo é usado em seguida para todas as operações de desenho necessárias para criar a imagem. Quando o sistema processa uma função GDI associada a um DC de metarquivo, ele converte a função nos dados apropriados e armazena esses dados em um registro anexado ao metarquivo.

Depois que uma imagem for concluída e o último registro for armazenado no metarquivo, você poderá passar o metarquivo para outro aplicativo:

-   Usando a área de transferência
-   Inserindo-o em outro arquivo
-   Armazenando em disco
-   Jogando repetidamente

Um metarquivo é *reproduzido* quando seus registros são convertidos em comandos de dispositivo e processados pelo dispositivo apropriado.

Há dois tipos de metaarquivos:

-   [Metarquivos de formato avançado](enhanced-format-metafiles.md)
-   [metaarquivos de formato Windows](windows-format-metafiles.md)

 

 



