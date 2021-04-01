---
description: Habilita a capacidade de executar o reconhecimento de tinta, recuperar o resultado do reconhecimento e recuperar alternativas. O InkRecognizerContext permite que vários reconhecedores instalados em um sistema usem o reconhecimento de tinta para processar a entrada adequadamente.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: Classe InkRecognizerContext (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerContext
- InkRecognizerContext.IInkRecognizerContext
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: afe5469cabf6764ed9b02fdcffcc8c1bedaca1d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169899"
---
# <a name="inkrecognizercontext-class"></a>Classe InkRecognizerContext

Habilita a capacidade de executar o reconhecimento de tinta, recuperar o resultado do reconhecimento e recuperar alternativas. O **InkRecognizerContext** permite que vários reconhecedores instalados em um sistema usem o reconhecimento de tinta para processar a entrada adequadamente.

**InkRecognizerContext** tem estes tipos de membros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

A classe **InkRecognizerContext** tem esses eventos.



| Evento                                                                               | Descrição                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconhecimento**](inkrecognizercontext-recognition.md)                             | Ocorre quando o InkRecognizerContext gerou resultados do método BackgroundRecognize.<br/>                                                                                             |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Ocorre quando o **InkRecognizerContext** gerou resultados depois de chamar o método [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="interfaces"></a>Interfaces

A classe **InkRecognizerContext** define essas interfaces.



| Interface                 | Descrição                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **IInkRecognizerContext** | Esse objeto implementa a interface com do **IInkRecognizerContext** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **InkRecognizerContext** tem esses métodos.



| Método                                                                                              | Descrição                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Especifica que o reconhecedor deve reconhecer os traços associados e acionar um evento de [**reconhecimento**](inkrecognizercontext-recognition.md) quando o reconhecimento for concluído.<br/>                                                                |
| [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Especifica que o reconhecedor deve reconhecer os traços associados e disparar um evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) quando o reconhecimento for concluído.<br/>                                    |
| [**8i**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Cria um **InkRecognizerContext** duplicado.<br/>                                                                                                                                                                                               |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Encerra a entrada de tinta para o **InkRecognizerContext**.<br/>                                                                                                                                                                                             |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Indica se o dicionário do sistema, o dicionário do usuário ou a [**lista de palavras**](inkwordlist-class.md) contêm uma cadeia de caracteres especificada.<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Executa o reconhecimento em uma coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e retorna resultados de reconhecimento.<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Encerra o reconhecimento em segundo plano que foi iniciado com uma chamada para [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) ou [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates).<br/> |



 

### <a name="properties"></a>Propriedades

A classe **InkRecognizerContext** tem essas propriedades.



| Propriedade                                                                                   | Tipo de acesso           | Descrição                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Leitura/gravação<br/> | Obtém ou define o modo de preenchimento automático de caractere, que determina quando caracteres ou palavras são reconhecidos.<br/>                                         |
| [**Facto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Leitura/gravação<br/> | Obtém ou define o nome da cadeia de caracteres do factor usado pelo objeto **InkRecognizerContext** .<br/>                                                        |
| [**Guia**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Leitura/gravação<br/> | Obtém ou define o [**InkRecognizerGuide**](inkrecognizerguide-class.md) a ser usado para entrada à tinta.<br/>                                                   |
| [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Leitura/gravação<br/> | Obtém ou define os caracteres que vêm antes da coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) no objeto **InkRecognizerContext** .<br/> |
| [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Leitura/gravação<br/> | Obtém ou define os sinalizadores que especificam como o reconhecedor interpreta a tinta e determina a cadeia de caracteres de resultado.<br/>                                     |
| [**Reconhecedor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Leitura/gravação<br/> | Obtém ou define o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) usado pelo objeto **InkRecognizerContext** .<br/>                                   |
| [**Traços**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Leitura/gravação<br/> | Obtém ou define a coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) associada ao objeto **InkRecognizerContext** .<br/>                    |
| [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Leitura/gravação<br/> | Obtém ou define os caracteres que vêm após a coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) no objeto **InkRecognizerContext** .<br/>  |
| [**Palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Leitura/gravação<br/> | Obtém ou define o objeto [**InkWordList**](inkwordlist-class.md) usado para melhorar os resultados de reconhecimento.<br/>                               |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

Há dois tipos de reconhecimento: plano de fundo (assíncrono) ou de primeiro plano (síncrono). O reconhecimento em segundo plano é iniciado por uma chamada para os métodos [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) ou [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) , ocorre em um thread em segundo plano e relata os resultados para o aplicativo por meio de um mecanismo de evento. O reconhecimento de primeiro plano não retorna até que todo o reconhecimento seja concluído, tornando os resultados de reconhecimento disponíveis para o thread de chamada sem escutar o evento de reconhecimento.

A tinta é processada continuamente em segundo plano. Se um [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for adicionado à coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) à qual o **InkRecognizerContext** se refere, então o **IInkStrokeDisp** será reconhecido imediatamente. Consulte comentários no tópico do método [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) para obter mais detalhes.

Todo o reconhecimento ocorre por meio de um contexto de reconhecedor. O contexto define as configurações para uma única sessão de reconhecimento. Ele recebe a tinta que deve ser reconhecida e define as restrições na entrada de tinta e na saída de reconhecimento. As restrições que podem ser definidas no contexto incluem o idioma, o dicionário e a gramática que está sendo usada.

> [!Note]  
> A configuração de propriedades diferentes das propriedades [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) ou [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) terá sucesso somente se a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) for **nula**. Você deve definir as outras propriedades antes de anexar a coleção InkStrokes ao **InkRecognizerContext**, ou você deve definir a coleção InkStrokes como **NULL** e, em seguida, definir as outras propriedades. Se você definir a coleção InkStrokes como **NULL** e, em seguida, definir as outras propriedades, talvez seja necessário anexar novamente a coleção InkStrokes. Isso ocorre porque o reconhecimento começa logo depois que você atribui o InkStrokes ao **InkRecognizerContext**. Quando uma chamada é feita para [**reconhecer a \[ classe \] InkRecognizeContext do método**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) ou [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize), os resultados da chamada podem já estar disponíveis.

 

Para melhorar o desempenho do aplicativo, descarte seu objeto **InkRecognizerContext** quando ele não for mais necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[Coleção InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

