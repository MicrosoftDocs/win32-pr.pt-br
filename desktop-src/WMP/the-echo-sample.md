---
title: O exemplo de eco
description: O exemplo de eco
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- plug-ins Windows Media Player, visão geral do Echo sample
- plug-ins, visão geral do eco de exemplo
- plug-ins de processamento de sinal digital, visão geral do eco de exemplo
- Plug-ins do DSP, visão geral do eco de exemplo
- Guia de programação, plug-ins do DSP
- exemplos, plug-ins do DSP
- Exemplo de plug-in do eco DSP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103054e82157d83085713937759de8aa9ed250a5491146ebe0c71559ab1ca338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762786"
---
# <a name="the-echo-sample"></a>O exemplo de eco

o assistente de plug-in Windows Media Player pode criar um projeto de plug-in DSP para Microsoft Visual C++. O código padrão gerado pelo assistente permite que o usuário forneça um fator de escala entre 0 e 1, que é usado pelo programa como um multiplicador para os exemplos de áudio. essa é uma implementação muito simples que você pode estudar para entender como o Windows Media Player interage com plug-ins DSP. As informações na seção chamada [sobre plug-ins DSP](about-dsp-plug-ins.md) podem ajudá-lo a entender a implementação padrão.

O exemplo descrito nesta seção é um pouco mais complexo. Este exemplo permite que o usuário especifique um tempo de atraso, em milissegundos e um nível de efeito. O código usa esses valores para gerar um efeito de eco ao reproduzir arquivos que contêm áudio PCM (modulação de código de pulso). muitos dos tipos de arquivo que Windows Media Player renderizas usam áudio PCM.

Este guia é dividido nas seguintes seções:



| Seção                                                                                | Descrição                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Visão geral do eco de exemplo](echo-sample-overview.md)                                       | Descreve os requisitos gerais e as especificações do exemplo. Descreve como o plug-in funciona.              |
| [Propriedades de exemplo de eco](echo-sample-properties.md)                                   | Descreve como modificar a propriedade de código do assistente e adicionar métodos para a nova propriedade necessária para o exemplo de eco. |
| [Modificando a página de propriedades de exemplo de eco](modifying-the-echo-sample-property-page.md) | Mostra como modificar a implementação da página de propriedades existente para trabalhar com a amostra de eco.                         |
| [Trabalhando com recursos de streaming](working-with-streaming-resources.md)               | Demonstra como adicionar código para alocar e liberar um buffer necessário para o exemplo de eco.                                |
| [Implementando CEcho::D oProcessOutput](implementing-cecho--doprocessoutput.md)         | Descreve como implementar o código que cria o efeito de eco.                                                   |
| [Usando o plug-in DSP de exemplo Echo](using-the-echo-sample-dsp-plug-in.md)             | Descreve como usar o exemplo concluído.                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação de plug-ins do DSP**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




