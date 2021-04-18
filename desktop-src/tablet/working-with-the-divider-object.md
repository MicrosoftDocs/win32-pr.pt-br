---
description: O objeto divisória fornece acesso aos recursos de análise de layout do Tablet PC.
ms.assetid: 9fa299fe-3713-4fa8-95c6-be15f144103a
title: Trabalhando com o objeto divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd158f85d368d764bce17e8b481ebe625a4d6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810685"
---
# <a name="working-with-the-divider-object"></a>Trabalhando com o objeto divisor

O objeto [divisória](/previous-versions/ms583616(v=vs.100)) fornece acesso aos recursos de análise de layout do Tablet PC.

No código gerenciado, o objeto [divisória](/previous-versions/ms583616(v=vs.100)) pode ser instanciado chamando um dos construtores [divisórias](/previous-versions/ms839465(v=msdn.10)) . Na automação, isso é chamado de objeto [**InkDivider**](inkdivider-class.md) e pode ser instanciado chamando o método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

Você pode obter um instantâneo do resultado da análise atual chamando o método de [divisão](/previous-versions/ms839461(v=msdn.10)) do objeto [divisória](/previous-versions/ms583616(v=vs.100)) . O resultado da análise é retornado em um objeto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) . Cada vez que você chama o método divide, o objeto divisória cria um objeto DivisionResult. Para obter mais informações sobre o objeto DivisionResult, consulte [trabalhando com o objeto DivisionResult](working-with-the-divisionresult-object.md).

A coleção [Strokes](/previous-versions/ms552701(v=vs.100)) analisada pelo objeto [divisória](/previous-versions/ms583616(v=vs.100)) está contida na propriedade [Strokes](/previous-versions/ms839422(v=msdn.10)) do objeto divisória. O objeto divisória analisa dinamicamente a coleção Strokes à medida que você adiciona ou exclui da coleção. Para obter mais informações sobre a propriedade Strokes do objeto divisória, consulte [trabalhando com uma coleção de traços](working-with-a-strokes-collection.md).

O objeto [divisória](/previous-versions/ms583616(v=vs.100)) usa um contexto de reconhecedor para melhorar sua análise de segmentos de reconhecimento e gerar texto de reconhecimento para elementos de manuscrito. Você pode definir o contexto do reconhecedor usando a propriedade [RecognizerContext](/previous-versions/ms839415(v=msdn.10)) do objeto divisória. A Propriedade RecognizerContext não pode ser alterada após a atribuição de traços ao objeto divisória. Para obter mais informações sobre a Propriedade RecognizerContext do objeto divisória, consulte [trabalhando com um contexto de reconhecedor](working-with-a-recognizer-context.md).

> [!Caution]  
> No código gerenciado, você deve chamar o método [Dispose](/previous-versions/ms839450(v=msdn.10)) nesse objeto antes que ele saia do escopo. Este objeto mantém recursos não gerenciados. Depender da finalização desse objeto pode causar vazamentos de memória e exceções em seu aplicativo.

 

 

 
