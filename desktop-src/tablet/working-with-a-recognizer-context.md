---
description: O objeto divisória usa uma RecognizerContext para melhorar sua análise de segmentos de reconhecimento e gerar texto de reconhecimento para elementos de manuscrito.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Trabalhando com um contexto de reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010569"
---
# <a name="working-with-a-recognizer-context"></a>Trabalhando com um contexto de reconhecedor

O objeto [**divisória**](inkdivider-class.md) usa uma [**RecognizerContext**](inkrecognizercontext-class.md) para melhorar sua análise de segmentos de reconhecimento e gerar texto de reconhecimento para elementos de manuscrito.

Você pode definir o contexto do reconhecedor usando a propriedade [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) do objeto [**divisória**](inkdivider-class.md) ou fornecendo o contexto do reconhecedor na chamada para o construtor [divisória](/previous-versions/ms839465(v=msdn.10)) (em código gerenciado). Se um contexto de reconhecedor para um reconhecedor não manuscrito ou para um reconhecedor que não ofereça suporte à funcionalidade de entrada gratuita for atribuído à propriedade **RecognizerContext** , uma exceção será lançada.

Se os reconhecedores não estiverem instalados ou se um contexto de reconhecedor não for atribuído ao objeto [**divisória**](inkdivider-class.md) , o objeto **divisória** não usará um contexto de reconhecedor. Nesse caso, o recurso de análise de layout executa a divisão de segmento e nenhum texto é associado ao objeto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .

> [!Note]  
> A propriedade [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) não pode ser alterada após a atribuição de traços ao objeto [**divisória**](inkdivider-class.md) . O objeto **divisória** usa os valores de propriedade padrão do objeto [**RecognizerContext**](inkrecognizercontext-class.md) .

 

O objeto [**divisória**](inkdivider-class.md) aplica o contexto do reconhecedor a elementos manuscritos durante a análise de layout. Todos os traços que você atribui diretamente ao contexto do reconhecedor são ignorados pelo objeto **divisória** . Para obter mais informações sobre reconhecimento de texto, consulte [sobre o reconhecimento de manuscrito](about-handwriting-recognition.md).

 

 
