---
description: Como uma região de recorte, um caminho de clipe é outro objeto gráfico que um aplicativo pode selecionar em um contexto de dispositivo.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Caminhos de clipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967705"
---
# <a name="clip-paths"></a>Caminhos de clipes

Como uma região de recorte, um caminho de clipe é outro objeto gráfico que um aplicativo pode selecionar em um contexto de dispositivo. Ao contrário de uma região de recorte, um caminho de clipe é sempre criado por um aplicativo e é usado para recortar em uma ou mais formas irregulares. Por exemplo, um aplicativo pode usar as linhas e curvas que formam os contornos de caracteres em uma cadeia de caracteres de texto para definir um caminho de clipe.

Para criar um caminho de clipe, primeiro é necessário criar um caminho que descreva a forma irregular necessária. Os caminhos são criados chamando as funções de desenho da interface de dispositivo gráfico (GDI) apropriada depois de chamar a função [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) e antes de chamar a função [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Essa coleção de funções é chamada de colchete de caminho. Para obter mais informações sobre caminhos e colchetes de caminho, consulte [caminhos](paths.md).

Depois que o caminho é criado, ele pode ser convertido em um caminho de clipe chamando a função [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , identificando um contexto de dispositivo e especificando um modo de uso. O modo de uso determina como o sistema combina o novo caminho de clipe com a região de recorte original do contexto do dispositivo. A tabela a seguir descreve os modos de uso.



| Mode      | Descrição                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| RGN \_ e  | O caminho do clipe inclui a interseção (áreas sobrepostas) da região de recorte do contexto do dispositivo e o caminho atual.    |
| \_cópia RGN | O caminho do clipe é o caminho atual.                                                                                           |
| RGN \_ diff | O caminho do clipe inclui a região de recorte do contexto do dispositivo com qualquer parte de interseção do caminho atual excluído.        |
| RGN \_ ou   | O caminho do clipe inclui a União (áreas combinadas) da região de recorte do contexto do dispositivo e o caminho atual.              |
| \_XOR RGN  | O caminho do clipe inclui a União da região de recorte do contexto do dispositivo e o caminho atual, mas exclui a interseção. |



 

 

 



