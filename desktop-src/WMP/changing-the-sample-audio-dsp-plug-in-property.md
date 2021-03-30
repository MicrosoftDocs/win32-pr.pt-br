---
title: Alterando a propriedade de plug-in do DSP de áudio de exemplo
description: Alterando a propriedade de plug-in do DSP de áudio de exemplo
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Plug-ins do Windows Media Player, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, propriedades de áudio
- Plug-ins do DSP, propriedades de áudio
- plug-ins do DSP de áudio, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc27f58fa8c8903b54f9903797dcc32a7795841
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636463"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Alterando a propriedade de plug-in do DSP de áudio de exemplo

Você provavelmente vai querer alterar a propriedade que o assistente de plug-in do Windows Media Player cria por padrão. A lista a seguir detalha os itens que podem exigir alteração:

-   **O recurso de caixa de diálogo.** Clique na guia **ResourceView** na janela espaço de trabalho do projeto. Expanda a lista de pastas para abrir a pasta caixa de diálogo. Clique duas vezes no recurso de caixa de diálogo para abrir o editor de recursos. Você pode fazer alterações na caixa de diálogo da página de propriedades para atender às suas necessidades. Por exemplo, você pode alterar o texto no rótulo ou substituir o controle de edição por uma caixa de seleção.
-   **O código do objeto da página de propriedades.** A implementação padrão usa uma variável do tipo Double para armazenar o fator de escala. Você pode exigir um tipo diferente de dados. Isso também exigiria que você alterasse o código que persiste os dados no registro e leia os dados do registro (incluindo o código que lê do registro em *CProjectName*::**FinalConstruct**).
-   **A variável de membro que armazena o valor da propriedade.** Essa variável é denominada "m \_ fScaleFactor" e é declarada como tipo Double. Talvez você queira alterar o nome e o tipo dessa variável em todo o projeto.
-   **Os métodos get e Property Put da propriedade.** Talvez você queira alterar os nomes, os parâmetros e as implementações desses métodos. Não se esqueça de também refletir essas alterações em outro lugar no projeto. Por exemplo, o método de **aplicação** da página de propriedades chama **a \_ escala** *CProjectName*:: Put.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in do DSP de áudio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




