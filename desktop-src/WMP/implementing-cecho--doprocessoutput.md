---
title: Implementando CEcho DoProcessOutput
description: Implementando CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- plug-ins de Windows Media Player, método Echo de exemplo DoProcessOutput
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07054950cabadbc835c9904d48cdb4e6ddf5f05c0822c997558381958a9857d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135639"
---
# <a name="implementing-cechodoprocessoutput"></a>Implementando CEcho::D oProcessOutput

O método **DoProcessOutput** executa o processamento de sinal digital. Esse é o método que faz as alterações nos dados fornecidos pelo Windows Media Player. São os resultados desse método que você ouvirá como um efeito de eco quando o plug-in de exemplo de eco for concluído.

Para este exemplo, o plug-in processará apenas áudio de 8 ou 16 bits. Você precisará fazer algumas alterações no código de exemplo do assistente de plug-in para remover as seções que processam áudio de maior profundidade de bits. No entanto, vale a pena estudar essas seções, pois você pode decidir adicionar sua própria implementação de eco para esses formatos.

As seções a seguir detalham as alterações que você precisa fazer no código:

-   [Removendo o código para processar mais de 16 bits](removing-the-code-to-process-greater-than-16-bits.md)
-   [Processando os dados de áudio](processing-the-audio-data.md)
-   [Variáveis para executar o processamento](variables-to-perform-processing.md)
-   [Criando o efeito de eco](creating-the-echo-effect.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**O exemplo de eco**](the-echo-sample.md)
</dt> </dl>

 

 




