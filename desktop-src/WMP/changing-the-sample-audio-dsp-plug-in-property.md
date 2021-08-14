---
title: Alterando a propriedade de plug-in DSP de áudio de exemplo
description: Alterando a propriedade de plug-in DSP de áudio de exemplo
ms.assetid: 9e742bcd-cff8-422f-ad91-d8d46f15bdc4
keywords:
- Windows Media Player plug-ins, DSP de áudio
- plug-ins, DSP de áudio
- plug-ins de processamento de sinal digital, propriedades de áudio
- Plug-ins do DSP, propriedades de áudio
- plug-ins DSP de áudio, propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8aac1cf385f41e966bec51f19454308cf52697c995db4962a45486999ebae9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342619"
---
# <a name="changing-the-sample-audio-dsp-plug-in-property"></a>Alterando a propriedade de plug-in DSP de áudio de exemplo

É provável que você queira alterar a propriedade que o assistente Windows Media Player plug-in cria por padrão. A lista a seguir detalha os itens que podem exigir alteração:

-   **O recurso de caixa de diálogo.** Clique na **guia ResourceView** na janela Project Workspace. Expanda a lista de pastas para abrir a pasta Diálogo. Clique duas vezes no recurso de caixa de diálogo para abrir o editor de recursos. Você pode fazer alterações na caixa de diálogo da página de propriedades para atender às suas necessidades. Por exemplo, você pode alterar o texto no rótulo ou substituir o controle de edição por uma caixa de seleção.
-   **O código do objeto da página de propriedades.** A implementação padrão usa uma variável do tipo double para armazenar o fator de escala. Você pode exigir um tipo diferente de dados. Isso também exigirá que você altere o código que persiste os dados para o Registro e leia os dados do Registro (incluindo o código que lê do Registro em *CProjectName*::**FinalConstruct**).
-   **A variável de membro que armazena o valor da propriedade.** Essa variável é denominada "m \_ fScaleFactor" e é declarada como tipo double. Talvez você queira alterar o nome e o tipo dessa variável em todo o projeto.
-   **Os métodos get e property put.** Talvez você queira alterar os nomes, parâmetros e implementações desses métodos. Não se esqueça de também refletir essas alterações em outro lugar no projeto. Por exemplo, a página de propriedades **Aplicar método** chama *CProjectName*::**put \_ scale**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando um plug-in DSP de áudio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




