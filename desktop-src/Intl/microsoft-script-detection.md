---
description: O serviço de detecção de script ELS é chamado de detecção de script da Microsoft.
ms.assetid: daf9f549-1eff-4666-b777-227ec31fba30
title: Detecção de script da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd38b36cb409c1f03d84b9fc21f2fe4439b8152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090952"
---
# <a name="microsoft-script-detection"></a>Detecção de script da Microsoft

O serviço de detecção de script ELS é chamado de detecção de script da Microsoft. Esse serviço permite que os aplicativos detectem os scripts em que o texto é gravado. O equivalente do NLS (suporte ao idioma nacional) de um serviço de detecção de script é a função [GetStringScripts](/windows/desktop/api/Winnls/nf-winnls-getstringscripts) . No entanto, o serviço ELS também recupera os intervalos de texto que pertencem a cada sistema de escrita.

## <a name="input-to-microsoft-script-detection"></a>Entrada para a detecção de script da Microsoft

A entrada para o serviço de detecção de scripts da Microsoft é o texto UTF-16 para o qual o serviço determina os intervalos de script.

## <a name="output-of-microsoft-script-detection"></a>Saída da detecção de script da Microsoft

A saída do serviço de detecção de scripts da Microsoft é uma matriz de intervalos, cada um contendo uma cadeia de caracteres UTF-16 terminada em nulo com o nome especificado Unicode do sistema de gravação associado. O serviço relata os caracteres normais comuns (Zyyy) e herdados (Qaai) como pertencentes ao intervalo de script anterior. O início de caracteres comuns e herdados é relatado como pertencente ao próximo intervalo de script. Se todos os caracteres no texto de entrada forem comuns ou herdados, a saída do serviço será um intervalo único com a cadeia de caracteres vazia como seus dados.

## <a name="microsoft-script-detection-operation"></a>Operação de detecção de script da Microsoft

O serviço de detecção de scripts da Microsoft mapeia os pontos de código pertencentes ao intervalo comum para o sistema de escrita anterior. Como alternativa, o serviço pode mapear os pontos de código para o próximo sistema de escrita se os pontos de código estiverem no início da cadeia de caracteres de entrada. O aplicativo não precisa lidar com o intervalo comum.

## <a name="microsoft-script-detection-guid"></a>GUID de detecção de script da Microsoft

O GUID para o serviço Microsoft Detecção de Idioma é declarado em Elssrvc. h, conforme mostrado no código a seguir.


```C++
// {2D64B439-6CAF-4f6b-B688-E5D0F4FAA7D7}
static const GUID ELS_GUID_SCRIPT_DETECTION =
    { 0x2D64B439, 0x6CAF, 0x4F6B, { 0xB6, 0x88, 0xE5, 0xD0, 0xF4, 0xFA, 0xA7, 0xD7 } };
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os serviços lingüísticos estendidos](about-extended-linguistic-services.md)
</dt> </dl>

 

 



