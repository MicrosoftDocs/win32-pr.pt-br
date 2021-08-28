---
title: Entradas do sistema para compactadores, descompactadores e renderizadores
description: Entradas do sistema para compactadores, descompactadores e renderizadores
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- vídeo para Windows (VFW), entradas do sistema de compressor
- VFW (vídeo para Windows), entradas do sistema de compressor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0afa453603eacffe0db1b3a904709a096e638dc284aa64aa388968a0e555c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892556"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a>Entradas do sistema para compactadores, descompactadores e renderizadores

O sistema usa entradas no registro para localizar drivers VCM. Essas entradas estão na forma de códigos de 2 4 caracteres separados por um ponto. O primeiro código de quatro caracteres é definido pelo sistema e pode ser um dos seguintes:



| Código de quatro caracteres | Descrição                               |
|---------------------|-------------------------------------------|
| VIDC              | Identifica os compactadores e os descompactadores. |
| "VIDS"              | Identifica renderizadores de fluxo de vídeo.        |
| "TXTS"              | Identifica renderizadores de fluxo de texto.         |
| "AUDS"              | Identifica os manipuladores de fluxo de áudio.         |



 

Renderizadores personalizados podem definir seus próprios códigos de quatro caracteres.

O segundo código de quatro caracteres é definido pelo driver. Normalmente, o segundo código de quatro caracteres corresponde ao tipo de dados que o driver pode manipular.

Ao abrir um driver VCM, um aplicativo especifica o tipo de driver e o tipo de manipulador de dados necessário. Normalmente, essas informações vêm do cabeçalho de fluxo. O sistema tenta abrir o manipulador de dados especificado, mas se ele falhar, o sistema pesquisará o registro em busca de um driver que tenha o manipulador necessário.

Ao procurar o driver, o sistema tenta corresponder os códigos de quatro caracteres especificados para o tipo de driver e o manipulador de dados com os especificados na entrada do driver. Por exemplo, se um aplicativo especificar o compressor MSSQ, o sistema pesquisará o registro para a entrada de driver VIDC. MSSQ. Se não for possível encontrar uma correspondência, ele abrirá cada driver correspondente ao tipo de driver e localizará um que possa manipular o tipo de dados que seu aplicativo especifica. No exemplo anterior, se o sistema não pôde localizar VIDC. MSSQ, ele abriria todos os drivers com o código de quatro caracteres "VIDC" e localizará um que possa lidar com os dados.

 

 




