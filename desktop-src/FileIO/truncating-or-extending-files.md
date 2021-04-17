---
description: Um aplicativo pode truncar ou estender um arquivo chamando SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Truncando ou estendendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761728"
---
# <a name="truncating-or-extending-files"></a>Truncando ou estendendo arquivos

Um aplicativo pode truncar ou estender um arquivo chamando [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile). Essa função define o marcador de fim do arquivo para a posição atual do ponteiro do arquivo.

Observe que, quando um arquivo é estendido, o conteúdo entre os locais de fim de arquivo antigo e novo não é definido.

 

 



