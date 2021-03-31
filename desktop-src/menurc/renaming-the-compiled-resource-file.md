---
title: Renomeando o arquivo de recurso compilado
description: Por padrão, ao compilar recursos, o RC nomeia o arquivo de recurso compilado (. res) com o nome base do arquivo. rc e o coloca no mesmo diretório que o arquivo. rc.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159368"
---
# <a name="renaming-the-compiled-resource-file"></a>Renomeando o arquivo de recurso compilado

Por padrão, ao compilar recursos, o RC nomeia o arquivo de recurso compilado (. res) com o nome base do arquivo. rc e o coloca no mesmo diretório que o arquivo. rc. CVTRES deve ser chamado para converter o arquivo. res em um formato de recurso binário (. RBJ) que pode ser compreendido pelo vinculador. O exemplo a seguir compila MyApp. rc e cria um arquivo de recurso compilado chamado MyApp. res no mesmo diretório que MyApp. rc:

**RC MyApp. rc**

A opção **/fo** dá ao arquivo. res resultante um nome que difere do nome do arquivo. rc correspondente. Por exemplo, para nomear o arquivo. res NewFile. res, use o seguinte comando:

**RC-fo newfile. res MyApp. rc**

A opção **/fo** também pode posicionar o arquivo. res em um diretório diferente. Por exemplo, o comando a seguir coloca o arquivo de recurso compilado MyApp. res no diretório C \\ : \\ recurso de origem:

**RC-fo c: \\ recurso de origem \\ \\ MyApp. res MyApp. rc**

 

 




