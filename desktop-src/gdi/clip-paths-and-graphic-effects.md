---
description: Um aplicativo pode usar recorte e caminhos para criar efeitos gráficos especiais. A ilustração a seguir mostra uma cadeia de texto desenhada com uma fonte Arial grande.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Caminhos de clipes e efeitos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502435"
---
# <a name="clip-paths-and-graphic-effects"></a>Caminhos de clipes e efeitos gráficos

Um aplicativo pode usar recorte e caminhos para criar efeitos gráficos especiais. A ilustração a seguir mostra uma cadeia de texto desenhada com uma fonte Arial grande.

![ilustração mostrando texto preto em um plano de fundo branco](images/cspth-02.png)

A ilustração a seguir mostra o resultado da seleção do texto como um caminho de clipe e o desenho de linhas radiais para um círculo cujo centro está localizado acima e à esquerda da cadeia de caracteres.

![ilustração mostrando o mesmo texto, mas preenchido com linhas em vez de preto sólido](images/cspth-03.png)

> [!Note]  
> Antes da interface de dispositivo de gráficos (GDI) adicionar texto criado com uma fonte de bitmap a um caminho, ele converte a fonte em um contorno ou em uma fonte de vetor.

 

Um aplicativo cria um caminho de clipe gerando um colchete de caminho e, em seguida, chamando a função [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) . Depois que um caminho de clipe é selecionado em um DC, a saída aparece apenas dentro das bordas do caminho.

Além de criar efeitos gráficos especiais, os caminhos de clipes também são úteis em aplicativos que salvam imagens como metaarquivos aprimorados. Usando um caminho de clipe, um aplicativo é capaz de garantir a independência do dispositivo, pois as unidades usadas para especificar um caminho são unidades lógicas.

 

 



