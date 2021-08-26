---
description: Para editar uma imagem armazenada em um metadado avançado, um aplicativo deve executar as tarefas descritas no procedimento a seguir.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Editando um metadado aprimorado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a052be915d966d90a0189376de7e1ff6e27831ebc9c44a0ff6af266b37fa65f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015576"
---
# <a name="editing-an-enhanced-metafile"></a>Editando um metadado aprimorado

Para editar uma imagem armazenada em um metadado avançado, um aplicativo deve executar as tarefas descritas no procedimento a seguir.

**Para editar uma imagem armazenada em um metadado aprimorado**

1.  Use o teste de acerto para capturar as coordenadas do cursor e recuperar a posição do objeto (linha, arco, retângulo, elipse, polígono ou forma irregular) que o usuário deseja alterar.
2.  Converta essas coordenadas em unidades lógicas (ou mundo).
3.  Chame a [**função EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) e examine cada registro de metadados.
4.  Determine se um determinado registro corresponde a uma função de desenho GDI.
5.  Se isso acontecer, determine se as coordenadas armazenadas no registro correspondem à linha, ao arco, à elipse ou a outro elemento gráfico que cruza as coordenadas especificadas pelo usuário.
6.  Ao localizar o registro que corresponde à saída que o usuário deseja alterar, apague o objeto na tela que corresponde ao registro original.
7.  Exclua o registro correspondente do metarquivo, salvando um ponteiro em seu local.
8.  Permitir que o usuário redesenhar ou substituir o objeto.
9.  Converta as funções GDI usadas para desenhar o novo objeto em um ou mais registros de metadados aprimorados.
10. Armazene esses registros no metadado aprimorado.

 

 



