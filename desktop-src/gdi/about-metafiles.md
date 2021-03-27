---
description: Internamente, um metarquivo é uma matriz de estruturas de comprimento variável chamada registros de metarquivo.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Sobre os metaarquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647673"
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
-   [Metaarquivos de formato do Windows](windows-format-metafiles.md)

 

 



