---
description: Permite a capacidade de executar o reconhecimento de tinta, recuperar o resultado do reconhecimento e recuperar alternativas. O InkRecognizerContext permite que os vários reconhecedores instalados em um sistema usem o reconhecimento de tinta para processar a entrada adequadamente.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: Classe InkRecognizerContext (Msinkaut.h)
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
ms.openlocfilehash: 781d1b440f1287b22d5c3ddf7ecf7132f7311fc5f48da5da20e4145717f65bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218397"
---
# <a name="inkrecognizercontext-class"></a>Classe InkRecognizerContext

Permite a capacidade de executar o reconhecimento de tinta, recuperar o resultado do reconhecimento e recuperar alternativas. O **InkRecognizerContext** permite que os vários reconhecedores instalados em um sistema usem o reconhecimento de tinta para processar a entrada adequadamente.

**InkRecognizerContext** tem estes tipos de membros:

-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

A **classe InkRecognizerContext** tem esses eventos.



| Evento                                                                               | Descrição                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconhecimento**](inkrecognizercontext-recognition.md)                             | Ocorre quando InkRecognizerContext gerou resultados do método BackgroundRecognize.<br/>                                                                                             |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Ocorre quando o **InkRecognizerContext** gerou resultados depois de chamar o [**método BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="interfaces"></a>Interfaces

A **classe InkRecognizerContext** define essas interfaces.



| Interface                 | Descrição                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **Iinkrecognizercontext** | Esse objeto implementa a interface **COM IInkRecognizerContext.**<br/> |



 

### <a name="methods"></a>Métodos

A **classe InkRecognizerContext** tem esses métodos.



| Método                                                                                              | Descrição                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Especifica que o reconhecedor deve reconhecer os traços associados e disparar um evento [**de**](inkrecognizercontext-recognition.md) Reconhecimento quando o reconhecimento for concluído.<br/>                                                                |
| [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Especifica que o reconhecedor deve reconhecer os traços associados e disparar um evento [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) quando o reconhecimento for concluído.<br/>                                    |
| [**Clone**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Cria um **InkRecognizerContext duplicado.**<br/>                                                                                                                                                                                               |
| [**EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Termina a entrada de tinta **para InkRecognizerContext.**<br/>                                                                                                                                                                                             |
| [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Indica se o dicionário do sistema, o dicionário de usuário ou a lista [**de**](inkwordlist-class.md) palavras contêm uma cadeia de caracteres especificada.<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Executa o reconhecimento em uma [**coleção InkStrkes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e retorna resultados de reconhecimento.<br/>                                                                                                                          |
| [**StopBackgroundRecognition**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Encerra o reconhecimento em segundo plano que foi iniciado com uma chamada para [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) ou [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates).<br/> |



 

### <a name="properties"></a>Propriedades

A **classe InkRecognizerContext** tem essas propriedades.



| Propriedade                                                                                   | Tipo de acesso           | Descrição                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Leitura/gravação<br/> | Obtém ou define o modo de preenchimento automático do caractere, que determina quando caracteres ou palavras são reconhecidos.<br/>                                         |
| [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Leitura/gravação<br/> | Obtém ou define o nome da cadeia de caracteres do factoid usado pelo **objeto InkRecognizerContext.**<br/>                                                        |
| [**Guia**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Leitura/gravação<br/> | Obtém ou define [**o InkRecognizerGuide a**](inkrecognizerguide-class.md) ser usado para entrada de tinta.<br/>                                                   |
| [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Leitura/gravação<br/> | Obtém ou define os caracteres que vêm antes da [**coleção InkStrkes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) no **objeto InkRecognizerContext.**<br/> |
| [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Leitura/gravação<br/> | Obtém ou define os sinalizadores que especificam como o reconhecedor interpreta a tinta e determina a cadeia de caracteres de resultado.<br/>                                     |
| [**Reconhecedor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Leitura/gravação<br/> | Obtém ou define [**o objeto IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) usado pelo **objeto InkRecognizerContext.**<br/>                                   |
| [**Traços**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Leitura/gravação<br/> | Obtém ou define a [**coleção InkStrkes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) associada ao **objeto InkRecognizerContext.**<br/>                    |
| [**SufixoTexto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Leitura/gravação<br/> | Obtém ou define os caracteres que vêm após a [**coleção InkStrkes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) no **objeto InkRecognizerContext.**<br/>  |
| [**Wordlist**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Leitura/gravação<br/> | Obtém ou define o [**objeto InkWordList**](inkwordlist-class.md) usado para melhorar os resultados de reconhecimento.<br/>                               |



 

## <a name="remarks"></a>Comentários

Esse objeto pode ser instanado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.

Há dois tipos de reconhecimento: em segundo plano (assíncrono) ou em primeiro plano (síncrono). O reconhecimento em segundo plano é iniciado por uma chamada para os métodos [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) ou [**BackgroundRecognizeWithAlternates,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) ocorre em um thread em segundo plano e relata os resultados para o aplicativo por meio de um mecanismo de evento. O reconhecimento em primeiro plano não retorna até que todo o reconhecimento seja concluído, disponibilizando assim os resultados de reconhecimento para o thread de chamada sem escutar o evento de reconhecimento.

A tinta é processada continuamente em segundo plano. Se [**um IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for adicionado à coleção [InkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) à qual **o InkRecognizerContext** se refere, **o IInkRogkeDisp** será reconhecido imediatamente. Consulte comentários no tópico [**do método EndInkInput**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) para obter mais detalhes.

Todo o reconhecimento ocorre por meio de um contexto de reconhecedor. O contexto define as configurações de uma única sessão de reconhecimento. Ele recebe a tinta que deve ser reconhecida e define as restrições na entrada de tinta e na saída de reconhecimento. As restrições que podem ser definidas no contexto incluem a linguagem, o dicionário e a gramática que está sendo usada.

> [!Note]  
> Definir propriedades diferentes das propriedades [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) ou [**CharacterAutoCompletion**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) só terá êxito se a [coleção InkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) for **NULL.** Você deve definir as outras propriedades antes de anexar a coleção InkStrkes ao **InkRecognizerContext** ou definir a coleção InkStrkes como **NULL** e, em seguida, definir as outras propriedades. Se você definir a coleção InkStrkes como **NULL** e, em seguida, definir as outras propriedades, talvez seja preciso reattar a coleção InkStrkes. Isso acontece porque o reconhecimento é iniciado logo depois que você atribui o InkStrkes ao **InkRecognizerContext.** Quando uma chamada é feita para [**a Classe \[ InkRecognizeContext do \]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) Método recognize ou [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize), os resultados da chamada podem já estar disponíveis.

 

Para melhorar o desempenho do aplicativo, descarte o objeto **InkRecognizerContext** quando ele não for mais necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut.h (também requer Msinkaut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IInkRecognizer Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[Coleção InkStrkes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

