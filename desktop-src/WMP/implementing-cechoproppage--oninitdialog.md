---
title: Implementando CEchoPropPage OnInitDialog
description: Implementando CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, método CEchoPropPage OnInitDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105813153"
---
# <a name="implementing-cechoproppageoninitdialog"></a>Implementando CEchoPropPage:: OnInitDialog

O método **CEchoPropPage:: OnInitDialog** é implementado em EchoPropPage. cpp. Ele é executado quando a caixa de diálogo página de propriedades é chamada. O código nesse método precisa recuperar os valores de propriedade atuais e exibi-los na caixa de edição correta. O código de exemplo do assistente de plug-in fornece uma implementação para uma única propriedade. Você pode modificar esse código para uma das propriedades de exemplo de eco e, em seguida, adicionar o código para recuperar o segundo valor da propriedade.

## <a name="declaring-the-oninitdialog-method-variables"></a>Declarando as variáveis do método OnInitDialog

Primeiro, você deve remover a declaração de fScaleFactor e substituí-la pelas seguintes declarações de variável:


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a>Recuperando os valores atuais do plug-in

O código deve tentar recuperar os valores de propriedade atuais do plug-in de eco. O exemplo a seguir tenta recuperar cada propriedade:


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



A caixa de diálogo exibe o valor de nível de efeitos para o usuário como um inteiro, mas o plug-in armazena o valor como um número de ponto flutuante. Portanto, o código converte o valor de ponto flutuante em um valor **DWORD** .

## <a name="retrieving-the-current-values-from-the-registry"></a>Recuperando os valores atuais do registro

Se a página de propriedades não puder recuperar os valores atuais do plug-in, ele deverá tentar lê-los no registro. O código a seguir lê cada valor de propriedade:


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



Observe o uso das constantes do registro que você criou anteriormente.

## <a name="displaying-the-values-to-the-user"></a>Exibindo os valores para o usuário

Por fim, a página de propriedades deve exibir os valores nos controles corretos da caixa de edição. O código de exemplo a seguir demonstra isso:


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modificando a página de propriedades de exemplo de eco**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




