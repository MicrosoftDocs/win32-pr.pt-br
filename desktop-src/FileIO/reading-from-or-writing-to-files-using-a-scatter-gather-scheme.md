---
description: Descreve um esquema de dispersão-coleta para leitura ou gravação de partes não contíguas de dados em uma única operação.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Lendo ou gravando em arquivos usando um esquema de Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778770"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a>Lendo ou gravando em arquivos usando um esquema de Scatter-Gather

Um esquema de coleta de dispersão usa o sistema operacional para entregar em uma operação várias partes discretas de dados (como registros de banco de dado) de um arquivo para separar buffers não contíguos na memória. Um esquema de dispersão e coleta também grava os dados de buffers não contíguos em uma operação.

Um aplicativo pode implementar um esquema de coleta de dispersão usando as funções [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .

 

 



