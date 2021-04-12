---
title: Composições
description: Uma composição é um estado de entrada temporário que permite que um serviço de texto especifique tanto para o aplicativo quanto para o usuário que o texto de entrada ainda está em um estado de alteração.
ms.assetid: 3d9da4f2-ceb9-4abc-8979-d3756d948a57
keywords:
- TSF (estrutura de serviços de texto), composições
- TSF (estrutura de serviços de texto), composições
- serviços de texto, composições
- Aplicativos habilitados para TSF, composições
- compositions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b03f3e991f76ee7c6dca3830267796576c7b842
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366488"
---
# <a name="compositions"></a>Composições

Uma composição é um estado de entrada temporário que permite que um serviço de texto especifique tanto para o aplicativo quanto para o usuário que o texto de entrada ainda está em um estado de alteração. Um aplicativo pode e deve obter informações de atributo de exibição sobre a composição e usar essas informações para exibir o estado de composição para o usuário.

Um exemplo do uso de uma composição é durante a entrada de fala. Enquanto o usuário está falando, o serviço de texto de fala cria uma composição. Essa composição permanecerá intacta até que toda a entrada de fala seja concluída. Quando a sessão termina, o serviço de texto de fala termina a composição.

Um aplicativo usa a presença e a ausência de uma composição para determinar como exibir texto e o que, se houver, o processamento deve ser executado no texto. Por exemplo, se o usuário estiver usando o mecanismo de fala para inserir texto, o aplicativo não deverá executar nenhuma verificação ortográfica ou gramatical em nenhum texto de composição. O texto é considerado incompleto até que a composição seja encerrada.

## <a name="text-services"></a>Serviços de texto

Um serviço de texto cria uma composição chamando [ITfContextComposition:: StartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition). Opcionalmente, o serviço de texto pode implementar um objeto [ITfCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcompositionsink) que recebe notificações de eventos de composição. StartComposition retorna um objeto [ITfComposition](/windows/desktop/api/msctf/nn-msctf-itfcomposition) ao qual o serviço de texto mantém uma referência e usa para modificar e encerrar a composição. O serviço de texto encerra a composição chamando [ITfComposition:: endcomposição](/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition).

Se um serviço de texto for criar composições, ele também deverá dar suporte a atributos de exibição para permitir que um aplicativo exiba o texto que faz parte de uma composição diferente do texto padrão. Para obter mais informações, consulte [fornecendo atributos de exibição](providing-display-attributes.md).

## <a name="applications"></a>Aplicativos

Um aplicativo pode monitorar a criação, a alteração e o encerramento de composições instalando um coletor [ITfContextOwnerCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink) . Quando uma composição é iniciada, [ITfContextOwnerCompositionSink:: OnStartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition) é chamado. Da mesma forma, quando uma composição é alterada ou terminada, [ITfContextOwnerCompositionSink:: OnUpdateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onupdatecomposition) e [ITfContextOwnerCompositionSink:: OnEndComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition) será chamado, respectivamente.

Veja a seguir um procedimento típico para atualizar um documento usando uma composição.

1.  [ITextStoreACP:: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection) ou [ITextStoreAnchor:: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection) normalmente são usados para inserir o texto inicial na composição.
2.  A composição é iniciada com uma chamada para [ITfContextComposition:: StartComposition](/windows/desktop/api/Msctf/nf-msctf-itfcontextcomposition-startcomposition), usando o intervalo de texto retornado por **InsertTextAtSelection**.
3.  Quando recebe uma nova entrada, como entrada de teclado ou fala, o aplicativo atualiza a composição com [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext) ou [ITextStoreAnchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext).
4.  Quando o aplicativo determina que é hora de encerrar a composição, ele chama [ITfComposition:: endcomposição](/windows/desktop/api/Msctf/nf-msctf-itfcomposition-endcomposition).

O aplicativo deve usar os atributos de exibição fornecidos pelo serviço de texto para modificar a exibição do texto em todos os momentos e não apenas quando uma composição estiver ativa. Para obter mais informações, consulte [usando atributos de exibição](using-display-attributes.md).

Se necessário, um aplicativo pode encerrar uma composição chamando [ITfContextOwnerCompositionServices:: TerminateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionservices-terminatecomposition).

 

 