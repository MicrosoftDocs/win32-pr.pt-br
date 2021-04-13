---
description: Todo o reconhecimento de controles habilitados para tinta ocorre por meio de um objeto RecognizerContext. As APIs de tecnologia do Tablet PC permitem definir a propriedade factoid em um objeto RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Configurando contexto para controles de Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297374"
---
# <a name="setting-context-for-ink-enabled-controls"></a>Configurando contexto para controles de Ink-Enabled

Todo o reconhecimento de controles habilitados para tinta ocorre por meio de um objeto [**RecognizerContext**](inkrecognizercontext-class.md) . As APIs de tecnologia do Tablet PC permitem definir a propriedade [**factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) em um objeto **RecognizerContext** .

Se você estiver criando um aplicativo habilitado para tinta, use as propriedades de [**facto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) e lista de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) para definir contextos.

Você pode passar os valores de cadeia de caracteres dos nomes nos escopos de entrada definidos na enumeração [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) para a propriedade [**factor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) , delimitada com uma abertura (! e um fechamento). Por exemplo, para definir o contexto de um objeto [**RecognizerContext**](inkrecognizercontext-class.md) com tendência de caracteres usados em uma URL, use a sintaxe mostrada nos exemplos C a seguir \# :


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> Os escopos de entrada, conforme definido na enumeração [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , substituem as entradas que estavam disponíveis nas versões anteriores do SDK do Windows XP Tablet PC Edition, embora essas paraestas continuem a funcionar para fornecer compatibilidade com versões anteriores.

 

O exemplo C a seguir \# define a propriedade [**factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) para CEPs:


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



Você pode combinar escopos de entrada usando a sintaxe de expressão regular de manuscrito. Para obter mais detalhes sobre como usar a sintaxe de expressão regular, consulte [escopos de entrada personalizados com expressões regulares](custom-input-scopes-with-regular-expressions.md).

Você pode definir sinalizadores de reconhecimento no objeto [**RecognizerContext**](inkrecognizercontext-class.md) para afetar o comportamento do reconhecedor. Um desses sinalizadores é o sinalizador de **coerção** na enumeração [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) de **RecognizerContext**. O sinalizador de **coerção** força o reconhecedor a retornar um resultado que corresponda à definição do factor definido. Por exemplo, se você tiver um formulário que exige que o usuário insira uma quantidade numérica, pode ser útil definir o factor de **\_ número is** e também definir a propriedade [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) para **coerção**. Nessa instância, o sinalizador de **coerção** garante que o reconhecedor retorne apenas números.

O exemplo C a seguir \# define a propriedade [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) para **coerção**:


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



No entanto, tome cuidado ao decidir definir o sinalizador de **coerção** . O sinalizador força o reconhecedor a corresponder apenas à definição do factor. Por exemplo, se você definir o \_ escopo de \_ entrada FULLTELEPHONENUMBER de telefone e o sinalizador de **coerção** , o reconhecedor retornará resultados que correspondam exatamente à definição de somente o escopo de \_ entrada de telefone \_ FULLTELEPHONENUMBER. Se um usuário gravar "911" com o \_ escopo de \_ entrada FULLTELEPHONENUMBER de telefone e o sinalizador de **coerção** definido, o reconhecedor poderá retornar uma cadeia de caracteres vazia ou uma cadeia de caracteres aleatória no formato (xxx) xxx-xxxx (em que X é um dígito). O formato XXX não corresponde à definição do FULLTELEPHONENUMBER de telefone IS \_ \_ , embora seja um número de telefone válido.

Para obter listas dos formatos com suporte para cada escopo de entrada, consulte a referência de [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .

Para retornar um campo para a configuração padrão para o reconhecedor, defina o facto como \_ padrão, como no exemplo C a seguir \# :


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



Para aplicativos que usam o controle [InkEdit](inkedit-control-reference.md) , defina o tipo de facto para o controle especificando:


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



Em que `IS_INPUTSCOPE` é o nome do escopo de entrada que você deseja aplicar.

O controle [InkEdit](inkedit-control-reference.md) não expõe um objeto [**RecognizerContext**](inkrecognizercontext-class.md) . Você ainda pode atribuir contexto usando a propriedade [**factoname**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) do controle InkEdit, mas não pode definir o sinalizador **WordMode** .

 

 
