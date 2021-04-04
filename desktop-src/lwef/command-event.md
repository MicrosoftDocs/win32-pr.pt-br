---
title: Evento de comando
description: Evento de comando
ms.assetid: 3e180286-dfa0-4b34-90ee-3267ed6f48af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5647e7eac3aaba0a6094be6b52cc3726eba34ad7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007517"
---
# <a name="command-event"></a>Evento de comando

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando o usuário escolhe um comando (do cliente).

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

 Comando de *subagente* \_  **(ByVal** *userinput * * *)**



| Parte        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Userinput* | Identifica o objeto de [**comando**](/windows/desktop/lwef/the-command-object) retornado pelo servidor. <br/> As propriedades a seguir podem ser acessadas no objeto de [**comando**](/windows/desktop/lwef/the-command-object) :<br/> Caractere de caracteres <br/> Um valor de cadeia de caracteres que identifica o nome (ID) do caractere que recebeu o comando. <br/> [**Nome**](name-property.md)<br/> Um valor de cadeia de caracteres que identifica o nome (ID) do comando.<br/> [**Confiança**](confidence-property.md)<br/> Um valor inteiro longo que indica a pontuação de confiança para o comando. <br/> [**Voz**](voice-property.md) <br/> Um valor de cadeia de caracteres que identifica o texto de voz do comando.<br/> Alt1Name <br/> Um valor de cadeia de caracteres que identifica o nome do próximo comando (segundo).<br/> Alt1Confidence <br/> Um valor inteiro longo que indica a pontuação de confiança para o próximo comando (segundo).<br/> Alt1Voice <br/> Um valor de cadeia de caracteres que identifica o texto de voz para a próxima correspondência de comando alternativo mais adequada.<br/> Alt2Name <br/> Um valor de cadeia de caracteres que identifica o nome da terceira melhor correspondência de comando.<br/> Alt2Confidence <br/> Um inteiro longo que identifica a pontuação de confiança para a terceira melhor correspondência de comando.<br/> Alt2Voice <br/> Um valor de cadeia de caracteres que identifica o texto de voz para a terceira melhor correspondência de comando.<br/> [**Contar**](count-property.md) <br/> Valor inteiro longo indicando o número de alternativas retornadas.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

O servidor o notificará com esse evento quando seu aplicativo estiver ativo e o usuário escolher um comando por meio do menu pop-up de entrada ou caractere falado. O evento retorna o número de possíveis comandos de correspondência em [**contagem**](count-property.md) , bem como o nome, a pontuação de confiança e o texto de voz para essas correspondências.

Se a entrada de voz disparar esse evento, o servidor retornará uma cadeia de caracteres que identifica a melhor correspondência no parâmetro de [**nome**](name-property.md) e a segunda e terceira-melhor correspondência em Alt1Name e Alt2Name. Uma cadeia de caracteres vazia indica que a entrada não correspondeu a nenhum comando definido pelo seu aplicativo; por exemplo, pode ser um dos comandos definidos do servidor. Se o comando foi correspondido ao comando do agente; por exemplo, ocultar, uma cadeia de caracteres vazia seria retornada no parâmetro **Name** , mas você ainda receberia o texto ouvido no parâmetro [**Voice**](voice-property.md) .

Você pode obter o mesmo nome de comando retornado em mais de uma entrada. Os parâmetros [**int**](confidence-property.md), Alt1Confidence e Alt2Confidence retornam as pontuações relativas, no intervalo de-100 a 100, que são retornados pelo mecanismo de reconhecimento de fala para cada correspondência correspondente. Os parâmetros [**Voice**](voice-property.md), Alt1Voice e Alt2Voice retornam o texto de voz que o mecanismo de reconhecimento de fala encontrou para cada alternativa. Se [**Count**](count-property.md) retornar zero (0), o servidor detectou entrada falada, mas determinou que não havia nenhum comando correspondente.

Se a entrada de voz não foi a origem do comando, por exemplo, se o usuário selecionou o comando no menu pop-up do caractere, o servidor retornará o nome (ID) do comando selecionado na propriedade [**nome**](name-property.md). Ele também retorna o valor do parâmetro de [**confiança**](confidence-property.md) como 100 e o valor dos parâmetros de [**voz**](voice-property.md) como a cadeia de caracteres vazia (""). Alt1Name e Alt2Name também retornam cadeias de caracteres vazias. Alt1Confidence e Alt2Confidence retornam zero (0) e Alt1Voice e Alt2Voice retornam cadeias de caracteres vazias. [**Count**](count-property.md) retorna 1.

> [!Note]  
> Nem todos os mecanismos de reconhecimento de fala podem retornar todos os valores para todos os parâmetros desse evento. Verifique com o fornecedor do mecanismo para determinar se o mecanismo oferece suporte à interface do Microsoft Speech API para retornar alternativas e pontuações de confiança.

 

 

