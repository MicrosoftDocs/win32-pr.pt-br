---
title: Como a amostra de eco persiste os dados
description: Como a amostra de eco persiste os dados
ms.assetid: be75760f-c378-45d1-99de-43ef0ec4b8f0
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df781754fd52639272850158187cb1258c081583
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636255"
---
# <a name="how-the-echo-sample-persists-data"></a>Como a amostra de eco persiste os dados

Quando o Windows Media Player habilita um plug-in do DSP, ele pode criar e destruir muitas instâncias do objeto de plug-in durante o curso de uma sessão. O plug-in precisa de uma maneira de manter seus valores de propriedade entre instâncias. O código de exemplo gerado pelo assistente de plug-in do Windows Media Player armazena esses valores no registro e os recupera quando a página de propriedades é invocada ou quando uma nova instância do plug-in é criada.

O código de exemplo padrão em Echo. h inclui duas constantes que armazenam o caminho de registro padrão e a cadeia de caracteres de nome do fator de escala. Você deve manter a variável que especifica o caminho, mas excluir a linha que especifica o nome do registro do fator de escala. Em seguida, adicione o código a seguir para definir constantes para o tempo de atraso e os nomes de propriedade de combinação úmida no registro. A seção concluído deve aparecer da seguinte maneira:


```C++
// registry location for preferences
const TCHAR kszPrefsRegKey[] = _T("Software\\Echo\\DSP Plugin");
const TCHAR kszPrefsDelayTime[] = _T("DelayTime");
const TCHAR kszPrefsWetmix[] = _T("Wetmix");

```



Você usará essas constantes ao modificar os métodos de página de propriedades.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modificando a página de propriedades de exemplo de eco**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




