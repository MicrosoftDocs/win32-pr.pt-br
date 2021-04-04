---
title: Usando o PlaySound para reproduzir sons do sistema
description: Usando o PlaySound para reproduzir sons do sistema
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- áudio de onda, função PlaySound
- áudio de formato de onda, tocando sons do sistema
- áudio de onda, eventos de som
- Função PlaySound, reproduzindo sons do sistema
- Função PlaySound, eventos de som
- reprodução de Wave-sons do sistema de áudio
- eventos de som
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823763"
---
# <a name="using-playsound-to-play-system-sounds"></a>Usando o PlaySound para reproduzir sons do sistema

A função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) também emitirá sons referidos por um KeyName no registro. Os usuários podem atribuir seus próprios sons a alertas e avisos do sistema ou a ações do usuário, como um clique no botão do mouse. Os sons associados a alertas do sistema e avisos são chamados de *eventos de som*.

Para reproduzir um evento de som, chame o **PlaySound** com o parâmetro *pszSound* apontando para uma cadeia de caracteres que contém o nome da entrada do registro que identifica o som. Por exemplo, para reproduzir o som associado à entrada "MouseClick" e aguardar a conclusão do som antes de retornar, use a seguinte instrução:


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



Se a entrada do Registro especificada ou o arquivo de wave-áudio identificado não existir, ou se o arquivo não couber na memória disponível, o **PlaySound** reproduzirá o som do sistema padrão.

Os eventos de som predefinidos pelo sistema podem variar com a plataforma. A lista a seguir fornece os eventos de som que são definidos para todas as implementações da API do Win32:

-   SystemAsterisk
-   SystemExclamation
-   SystemExit
-   SystemHand
-   SystemQuestion
-   SystemStart

Se um aplicativo registrar seus próprios eventos de som, o usuário poderá configurar o evento de som usando a interface padrão do painel de controle. O aplicativo deve registrar o evento de som usando as funções de registro padrão; para obter mais informações, consulte [registro](../sysinfo/registry.md). As entradas pertencem à mesma posição na hierarquia do registro como o restante dos eventos de som. Essa posição varia de acordo com a implementação do Win32. O valor de dados apropriado também varia de acordo com a implementação.

A função [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) sempre pesquisa o registro em busca de um KeyName correspondente a *lpszSound* antes de tentar carregar um arquivo com esse nome. A função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) aceita sinalizadores que especificam o local do som.

 

 