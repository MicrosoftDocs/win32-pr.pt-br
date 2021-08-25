---
description: Descreve um esquema de coleta de dispersão para ler ou escrever partes não contíguas de dados em uma única operação.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lendo ou escrevendo em arquivos usando um esquema de Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc8a7ee9fcae2a54ac31c51a7c038e3d9442a6ccded2fc7dab916c7a6165a68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914476"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Lendo ou escrevendo em arquivos usando um esquema de Scatter-Gather

Um esquema de coleta de dispersão usa o sistema operacional para entregar em uma operação várias partes discretas de dados (como registros de banco de dados) de um arquivo para buffers separados e não contíguos na memória. Um esquema de coleta de dispersão também grava os dados de buffers não contíguos em uma operação.

Um aplicativo pode implementar um esquema de coleta de dispersão usando as [**funções ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) e [**WriteFileGather.**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)

 

 



