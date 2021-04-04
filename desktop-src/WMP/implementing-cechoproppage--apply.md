---
title: Implementando CEchoPropPage Apply
description: Implementando CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Plug-ins do Windows Media Player, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins do DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do eco DSP, páginas de propriedades
- Exemplo de plug-in do eco DSP, método CEchoPropPage Apply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822717"
---
# <a name="implementing-cechoproppageapply"></a>Implementando CEchoPropPage:: apply

O método CEchoPropPage:: apply é implementado em EchoPropPage. cpp. Ele é executado quando o usuário clica em **aplicar** na caixa de diálogo página de propriedades no Windows Media Player. O código de exemplo do assistente de plug-in fornece uma implementação para lidar com uma única propriedade. Você pode modificar esse código para uma das propriedades de exemplo de eco e, em seguida, adicionar o código para armazenar o outro valor de propriedade.

## <a name="declaring-the-apply-method-variables"></a>Declarando as variáveis do método Apply

Primeiro, você deve remover a declaração de fScaleFactor. Em seguida, adicione declarações de variáveis que serão necessárias. O exemplo a seguir mostra as declarações de variável concluídas:


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Recuperando os valores da página de propriedades

Você deve implementar o código para recuperar e validar a entrada do usuário. O exemplo de código a seguir recupera o valor de tempo de atraso da \_ caixa de edição do DelayTime da IDC e, em seguida, verifica se o valor está dentro de um intervalo especificado:


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



Se a entrada do usuário não estiver no intervalo especificado, o código exibirá uma caixa de mensagem. Observe o uso do recurso de cadeia de caracteres que você criou anteriormente para a mensagem de erro.

O exemplo a seguir recupera o nível de efeito da \_ caixa de edição WETMIX do IDC e, em seguida, verifica se o valor está dentro de um intervalo especificado:


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a>Armazenando os valores de propriedade no registro

Em seguida, seu código deve manter os novos valores de propriedade no registro. O código a seguir armazena os dois valores de propriedade:


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a>Atualizando os valores de propriedade de plug-in de eco

O método **Apply** deve informar ao plug-in de eco que os valores de propriedade foram alterados. O código a seguir chama o método Property Put de cada propriedade usando o ponteiro de interface recuperado em CEchoPropPage:: SetObjects:


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



Observe que o valor de combinação úmida é convertido em ponto flutuante antes de ser passado para o plug-in.

## <a name="disabling-the-apply-button"></a>Desabilitando o botão aplicar

Como etapa final, seu código deve desabilitar a aplicação na caixa de diálogo página de propriedades como um sinal para o usuário que os valores foram atualizados com êxito. Isso requer uma única linha de código a seguir:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modificando a página de propriedades de exemplo de eco**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




