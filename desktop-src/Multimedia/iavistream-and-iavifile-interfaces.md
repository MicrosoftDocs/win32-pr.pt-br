---
title: Interfaces IAVIStream e IAVIFile
description: Interfaces IAVIStream e IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interface IAVIStream
- Interface IAVIFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822739"
---
# <a name="iavistream-and-iavifile-interfaces"></a>Interfaces IAVIStream e IAVIFile

As interfaces [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) e [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contêm os métodos usados por manipuladores de arquivo e de fluxo. O tipo de dados **PAVISTREAM** é um ponteiro para um objeto de fluxo AVI (por meio da interface **IAVIStream** ) e o tipo de dados **PAVIFILE** é um ponteiro para um objeto de arquivo AVI (por meio da interface **IAVIFile** ).

Para criar um ponteiro de objeto em C, primeiro aloque espaço para uma estrutura que seja grande o suficiente para conter o ponteiro para a tabela de função virtual e os outros membros de dados. Crie uma tabela de função virtual para os métodos para o tipo de fluxo e, em seguida, defina o ponteiro para a tabela de função virtual como o endereço da tabela de funções virtuais.

 

 




