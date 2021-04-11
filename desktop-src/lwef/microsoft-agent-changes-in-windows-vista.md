---
title: Alterações no Microsoft Agent no Windows Vista
description: Alterações no Microsoft Agent no Windows Vista
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73af45553f876c413fbea906de2369e888f1483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159943"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>Alterações no Microsoft Agent no Windows Vista

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

O Windows Vista apresenta algumas alterações na forma como o reconhecimento de fala e fala interage com o Windows Vista.

O Microsoft Agent agora dá suporte a componentes de reconhecimento de fala e de texto para fala do SAPI 5. As propriedades TTSModeID e SRModeID do objeto Agent ainda são usadas para determinar qual voz ou reconhecedor está selecionado para o agente e para alterar essa seleção. Os modos SAPI 4 aparecem como cadeias de caracteres GUID, como "{ca141fd0-ac7f-11D1-97a3-006008273000}", enquanto os tokens SAPI 5 (equivalentes aos modos) aparecem como nomes regulares, como "Microsoft Anna". Como em versões anteriores, o agente fará uma escolha padrão dos mecanismos TTS e SR. Se os mecanismos SAPI 5 estiverem instalados, eles serão sempre preferidos em todos os mecanismos SAPI 4 que podem ser instalados. O mecanismo de conversão de texto em fala padrão do usuário, conforme especificado no painel de controle, será usado se seu gênero corresponder ao do caractere; caso contrário, um mecanismo SAPI 5 do mesmo gênero será escolhido se um estiver disponível. As IDs de modo especificadas diretamente no caractere serão ignoradas se os mecanismos SAPI 5 estiverem presentes. As seleções padrão podem ser verificadas lendo as propriedades TTSModeID e SRModeID no início do script.

Como antes, TTSModeID e SRModeID retornará uma cadeia de caracteres em branco se o recurso de reconhecimento de fala ou de texto para fala não estiver presente. Um reconhecedor ou voz específico pode ser selecionado definindo essas propriedades para a cadeia de caracteres do modo SAPI 4 ou o nome do token SAPI 5 apropriado. Depois de definir um modo ou token específico, você também pode ler a propriedade novamente para verificar se seu valor foi obtido, o que indica que o novo modo ou token estava realmente disponível e foi selecionado com êxito. Para os desenvolvedores que implantam o agente pela Web, observe que muitos usuários do vista terão uma ou mais vozes SAPI 5 instaladas, portanto, convém evitar o download automático de vozes SAPI 4, a menos que o script solicite-as especificamente, pois a voz baixada não acabaria sendo usada.

Os mecanismos de conversão de texto em fala do SAPI 5 usam um conjunto diferente de padrões do que o SAPI 4 para anotar a fala com marcação, por exemplo, para alterar a densidade ou a taxa da fala. No SAPI 4, você usa comandos de "barra", como/Pit = 170/. No SAPI 5, você usa marcas XML, como <PITCH MIDDLE="5"/> . No Vista, o Agent aceitará os dois tipos de anotações nos comandos "barra" de cadeias de caracteres do método de fala serão ignorados por mecanismos do SAPI 5 e as marcas XML serão ignoradas pelos mecanismos do SAPI 4. Como com as marcas de barra, o suporte para marcas XML SAPI 5 varia de fornecedor para fornecedor e alguns fornecedores podem dar suporte a marcas adicionais. Para obter mais informações sobre marcas XML SAPI 5, consulte a especificação SAPI 5.

O Agent não inclui mais suporte para vários idiomas. O idioma usado pelo Agent sempre é considerado o idioma atual do usuário, como registrado no sistema operacional. A propriedade LanguageID do objeto Agent ainda é gravável, mas seu valor é ignorado pelo Agent no vista. Por exemplo, se o idioma do usuário estiver definido como inglês americano (&H0409), e ele usar um programa que defina LanguageID como francês (&H040C), o texto da dica de voz e as caixas de diálogo opções de caractere avançadas ainda aparecerão em inglês.

 

 




