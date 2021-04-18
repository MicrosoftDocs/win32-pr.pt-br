---
description: O serviço de detecção de idioma ELS é chamado de Microsoft Detecção de Idioma. Esse serviço usa a tecnologia patenteada pela Microsoft para permitir que os aplicativos detectem o idioma no qual o texto específico é escrito.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Detecção de Idioma da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785442"
---
# <a name="microsoft-language-detection"></a>Detecção de Idioma da Microsoft

O serviço de detecção de idioma ELS é chamado de Microsoft Detecção de Idioma. Esse serviço usa a tecnologia patenteada pela Microsoft para permitir que os aplicativos detectem o idioma no qual o texto específico é escrito.

## <a name="input-to-microsoft-language-detection"></a>Entrada para o Microsoft Detecção de Idioma

A entrada para o serviço Microsoft Detecção de Idioma é texto UTF-16 (forma normalizada C). O serviço precisa determinar o idioma deste texto.

## <a name="output-of-microsoft-language-detection"></a>Saída do Microsoft Detecção de Idioma

O serviço de Detecção de Idioma da Microsoft recupera as linguagens de listagem de cadeias de caracteres UTF-16 com final de nulo, representadas por seus nomes, separadas por delimitadores de caracteres nulos. A lista é classificada por relevância. Para a maioria dos idiomas, são usados nomes neutros. No entanto, para alguns, por exemplo, Sr-Cyrl, sr-latn, zh-Hant e zh-Hans, os nomes completos são usados.

## <a name="microsoft-language-detection-operation"></a>Operação do Microsoft Detecção de Idioma

O serviço Microsoft Detecção de Idioma verifica o script Unicode do texto fornecido pelo aplicativo. Ele segmenta o texto com base nos scripts que detecta e determina o idioma no qual cada segmento é gravado. Se um script indicar um único idioma, a linguagem terá a garantia de estar presente na lista de saída de idiomas. O serviço usa um algoritmo patenteado para determinar a relevância de cada idioma com suporte.

## <a name="microsoft-language-detection-guid"></a>GUID do Microsoft Detecção de Idioma

O GUID para o serviço Microsoft Detecção de Idioma é declarado em Elssrvc. h, conforme mostrado no código a seguir.


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os serviços lingüísticos estendidos](about-extended-linguistic-services.md)
</dt> </dl>

 

 



