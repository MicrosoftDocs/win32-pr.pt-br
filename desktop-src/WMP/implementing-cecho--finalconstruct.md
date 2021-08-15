---
title: Implementando CEcho FinalConstruct
description: Implementando CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- plug-ins Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, método CEcho FinalConstruct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeceeb9c0a7622ada62e98000ad4bfbc2e3faf08c22439039160810771cde8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748141"
---
# <a name="implementing-cechofinalconstruct"></a>Implementando CEcho:: FinalConstruct

O método CEcho:: FinalConstruct é implementado em Echo. cpp. ele contém o código para ler os valores de propriedade do registro quando Windows Media Player instancia o objeto de plug-in DSP. Isso é importante porque permite que as configurações do usuário persistam entre instâncias do objeto, bem como entre sessões. O código de exemplo do assistente de plug-in fornece implementação para ler uma única propriedade do registro. Você pode modificar esse código para manipular a propriedade de tempo de atraso e, em seguida, adicionar código para ler o valor da propriedade de combinação úmida.

O código de exemplo a seguir lê cada valor de Propriedade do registro e armazena cada um na variável de membro correta:


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



Observe que o valor DWORD para a combinação úmida é convertido em um valor de ponto flutuante. Observe também que o código calcula o valor correto para m \_ fDryMix.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modificando a página de propriedades de exemplo de eco**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




