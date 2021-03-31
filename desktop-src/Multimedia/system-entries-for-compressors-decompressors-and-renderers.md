---
title: Entradas do sistema para compactadores, descompactadores e renderizadores
description: Entradas do sistema para compactadores, descompactadores e renderizadores
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Vídeo para Windows (VFW), compressor entradas do sistema
- VFW (vídeo para Windows), entradas do sistema de compressor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636835"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a>Entradas do sistema para compactadores, descompactadores e renderizadores

O sistema usa entradas no registro para localizar drivers VCM. Essas entradas estão na forma de códigos de 2 4 caracteres separados por um ponto. O primeiro código de quatro caracteres é definido pelo sistema e pode ser um dos seguintes:



| Código de quatro caracteres | Description                               |
|---------------------|-------------------------------------------|
| VIDC              | Identifica os compactadores e os descompactadores. |
| "VIDS"              | Identifica renderizadores de fluxo de vídeo.        |
| "TXTS"              | Identifica renderizadores de fluxo de texto.         |
| "AUDS"              | Identifica os manipuladores de fluxo de áudio.         |



 

Renderizadores personalizados podem definir seus próprios códigos de quatro caracteres.

O segundo código de quatro caracteres é definido pelo driver. Normalmente, o segundo código de quatro caracteres corresponde ao tipo de dados que o driver pode manipular.

Ao abrir um driver VCM, um aplicativo especifica o tipo de driver e o tipo de manipulador de dados necessário. Normalmente, essas informações vêm do cabeçalho de fluxo. O sistema tenta abrir o manipulador de dados especificado, mas se ele falhar, o sistema pesquisará o registro em busca de um driver que tenha o manipulador necessário.

Ao procurar o driver, o sistema tenta corresponder os códigos de quatro caracteres especificados para o tipo de driver e o manipulador de dados com os especificados na entrada do driver. Por exemplo, se um aplicativo especificar o compressor MSSQ, o sistema pesquisará o registro para a entrada de driver VIDC. MSSQ. Se não for possível encontrar uma correspondência, ele abrirá cada driver correspondente ao tipo de driver e localizará um que possa manipular o tipo de dados que seu aplicativo especifica. No exemplo anterior, se o sistema não pôde localizar VIDC. MSSQ, ele abriria todos os drivers com o código de quatro caracteres "VIDC" e localizará um que possa lidar com os dados.

 

 




