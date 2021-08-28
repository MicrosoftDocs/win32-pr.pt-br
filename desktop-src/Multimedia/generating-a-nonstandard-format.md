---
title: Gerando um formato não padrão
description: Gerando um formato não padrão
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Gerenciador de compactação de áudio (ACM), formatos não padrão
- ACM (Gerenciador de compactação de áudio), formatos não padrão
- Exemplos do ACM, formatos não padrão
- função acmFormatSuggest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968dafae93cac419a0078989ab8786e02732cbaa942fd185969c5571c2e8237e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496336"
---
# <a name="generating-a-nonstandard-format"></a>Gerando um formato não padrão

Às vezes, um aplicativo precisa de um formato não padrão. Por exemplo, um aplicativo pode precisar de um arquivo de formato ADPCM de 16 kHz. Como 16 kHz não é padrão, as funções de enumeração não irão gerar esse formato. Na verdade, a codificação personalizada dos algoritmos de formato para o aplicativo não é uma maneira confiável de gerar um formato não padrão. Às vezes é possível, no entanto, gerar um formato análogo Configurando um formato PCM válido com todas as informações necessárias e, em seguida, usando a função [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) . Como os compactadores e os descompactadores tentam sugerir um formato mais próximo do formato desejado, o número de canais e a frequência são geralmente preservados.

 

 




