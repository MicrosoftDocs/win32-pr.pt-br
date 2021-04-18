---
description: O Tablet PC inclui tecnologia para reconhecer a entrada à tinta que é mais comum na forma de manuscrito.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Sobre o reconhecimento de manuscrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812006"
---
# <a name="about-handwriting-recognition"></a>Sobre o reconhecimento de manuscrito

O Tablet PC inclui tecnologia para reconhecer a entrada à tinta que é mais comum na forma de manuscrito. O módulo de software que fornece o reconhecimento é chamado de reconhecedor. Um reconhecedor reconhece uma linguagem, um grupo de idiomas relacionados ou uma classe de objetos relacionados, como notas musicais, gestos do sistema ou formas geométricas. Você pode adicionar reconhecedores dinamicamente ao sistema de serviços de tinta.

## <a name="recognition-steps"></a>Etapas de reconhecimento

O reconhecimento é tratado pelo uso de um contexto de reconhecedor. O reconhecimento consiste em quatro etapas básicas:

1.  Configurando as restrições de reconhecimento por:
    -   Selecionar o reconhecedor e o modo de entrada (restrições geométricas).
    -   Definindo as restrições de idioma. Por exemplo, você pode restringir a entrada para caracteres alfanuméricos ou pode passar esquemas para auxiliar o reconhecedor.
2.  Enviando tinta para o reconhecedor.
3.  Processando a entrada (reconhecendo).
4.  Retornando os resultados do reconhecimento.

As etapas 2 e 3 podem ser repetidas em um loop ou todos os traços de tinta podem ser adicionados à tinta antes da tentativa de reconhecimento.

## <a name="samples-and-related-topics"></a>Exemplos e tópicos relacionados

[Exemplo de reconhecimento avançado](advanced-recognition-sample.md) demonstra como usar os reconhecedores com objetos de [**tinta**](inkdisp-class.md) para executar o reconhecimento de tinta.

O [modelo de exemplo de DLL do Recognizer](recognizer-dll-sample-template.md) contém um modelo para criar uma DLL de reconhecimento. O modelo contém funções para registrar e cancelar o registro do servidor, bem como esqueletos para funções de reconhecedor primário.

As seções a seguir descrevem os conceitos básicos por trás da tecnologia de reconhecimento do Tablet PC. Para obter informações detalhadas sobre como criar Reconhecedores personalizados, consulte [criando um reconhecedor](creating-a-recognizer.md).

-   [Reconhecedores de texto](text-recognizers.md)
-   [Reconhecedores de objetos](object-recognizers.md)
-   [Usando a coleção Recognizers](using-the-recognizers-collection.md)
-   [Contexto do reconhecedor](recognizer-context.md)
-   [Segmentos de reconhecimento](recognition-segments.md)
-   [Reconhecimento de texto angular](recognition-of-angled-text.md)
-   [Suporte à reordenação de Stroke do Recognizer](recognizer-stroke-reordering-support.md)
-   [Dicionários e factos](dictionaries-and-factoids.md)
-   [Propriedade de confiança \[ sobre reconhecimento\]](confidence-property--about-recognition.md)
-   [Alternativos](alternates.md)
-   [Segmentos de tinta e alternativas](ink-segments-and-alternates.md)

 

 



