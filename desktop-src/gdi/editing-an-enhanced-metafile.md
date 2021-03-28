---
description: Para editar uma imagem armazenada em um metarquivo avançado, um aplicativo deve executar as tarefas descritas no procedimento a seguir.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Editando um metarquivo avançado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091188"
---
# <a name="editing-an-enhanced-metafile"></a>Editando um metarquivo avançado

Para editar uma imagem armazenada em um metarquivo avançado, um aplicativo deve executar as tarefas descritas no procedimento a seguir.

**Para editar uma imagem armazenada em um metarquivo avançado**

1.  Use o teste de impacto para capturar as coordenadas do cursor e recuperar a posição do objeto (linha, arco, retângulo, elipse, polígono ou forma irregular) que o usuário deseja alterar.
2.  Converta essas coordenadas em unidades lógicas (ou mundiais).
3.  Chame a função [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) e examine cada registro de metarquivo.
4.  Determine se um determinado registro corresponde a uma função de desenho GDI.
5.  Se tiver, determine se as coordenadas armazenadas no registro correspondem à linha, ao arco, à elipse ou a outros elementos gráficos que interseccionam as coordenadas especificadas pelo usuário.
6.  Ao localizar o registro que corresponde à saída que o usuário deseja alterar, apague o objeto na tela que corresponde ao registro original.
7.  Exclua o registro correspondente do metarquivo, salvando um ponteiro em seu local.
8.  Permitir que o usuário redesenhe ou substitua o objeto.
9.  Converta as funções GDI usadas para desenhar o novo objeto em um ou mais registros de metarquivo avançado.
10. Armazene esses registros no metarquivo avançado.

 

 



