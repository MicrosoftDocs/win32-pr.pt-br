---
description: O objeto Divider usa um RecognizerContext para melhorar sua análise de segmentos de reconhecimento e gerar texto de reconhecimento para elementos de manuscrito.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Trabalhando com um contexto de reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d99020e97170f0b68b1459abdc4b85f81ebc3fbba426233c2c13b5e042f28ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715094"
---
# <a name="working-with-a-recognizer-context"></a>Trabalhando com um contexto de reconhecedor

O [**objeto Divider**](inkdivider-class.md) usa [**um RecognizerContext**](inkrecognizercontext-class.md) para melhorar sua análise de segmentos de reconhecimento e gerar texto de reconhecimento para elementos de manuscrito.

Você pode definir o contexto do reconhecedor usando a propriedade [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) do objeto [**Divider**](inkdivider-class.md) ou fornecendo o contexto do reconhecedor na chamada para o construtor [Divisor](/previous-versions/ms839465(v=msdn.10)) (em código gerenciado). Se um contexto de reconhecedor para um reconhecedor não manuscrito ou para um reconhecedor que não dá suporte à funcionalidade de entrada livre for atribuído à propriedade **RecognizerContext,** uma exceção será lançada.

Se os reconhecedores não estão instalados ou um contexto de reconhecedor não é atribuído ao objeto [**Divider,**](inkdivider-class.md) o objeto **Divisor** não usa um contexto de reconhecedor. Nesse caso, o recurso de análise de layout executa a divisão de segmento e nenhum texto está associado ao [**objeto DivisionResult.**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)

> [!Note]  
> A [**propriedade RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) não pode ser alterada depois que os traços foram atribuídos ao [**objeto Divisor.**](inkdivider-class.md) O **objeto Divider** usa os valores de propriedade padrão do [**objeto RecognizerContext.**](inkrecognizercontext-class.md)

 

O [**objeto Divisor**](inkdivider-class.md) aplica o contexto do reconhecedor a elementos manuscritos durante a análise de layout. Todos os traços atribuídos diretamente ao contexto do reconhecedor são ignorados pelo **objeto Divisor.** Para obter mais informações sobre o reconhecimento de texto, consulte [Sobre o reconhecimento de manuscrito.](about-handwriting-recognition.md)

 

 
