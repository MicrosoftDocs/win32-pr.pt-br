---
title: Implementando CEchoPropPage Apply
description: Implementando CEchoPropPage Apply
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Windows Media Player plug-ins, páginas de propriedades de exemplo de eco
- plug-ins, páginas de propriedades de exemplo de eco
- plug-ins de processamento de sinal digital, páginas de propriedades de exemplo de eco
- Plug-ins DSP, páginas de propriedades de exemplo de eco
- Exemplo de plug-in do DSP de eco, páginas de propriedades
- Exemplo de plug-in echo DSP, método CEchoPropPage Apply
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a53d05bee90908f766034c300c99bcfa8d529b06e6713c803bd99bcf042b579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135619"
---
# <a name="implementing-cechoproppageapply"></a>Implementando CEchoPropPage::Apply

O método CEchoPropPage::Apply é implementado em EchoPropPage.cpp. Ele é executado quando o usuário clica em **Aplicar na** caixa de diálogo da página de propriedades no Windows Media Player. O código de exemplo do assistente de plug-in fornece uma implementação para lidar com uma única propriedade. Você pode modificar esse código para uma das propriedades de exemplo echo e, em seguida, adicionar código para armazenar o outro valor da propriedade.

## <a name="declaring-the-apply-method-variables"></a>Declarando as variáveis de método apply

Primeiro, você deve remover a declaração de fScaleFactor. Em seguida, adicione declarações de variável de que você precisará. O exemplo a seguir mostra as declarações de variável concluídas:


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>Recuperando os valores da página de propriedades

Você deve implementar o código para recuperar e validar a entrada do usuário. O exemplo de código a seguir recupera o valor de tempo de atraso da caixa de edição DELAYTIME do IDC e verifica se o valor está dentro de \_ um intervalo especificado:


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



Se a entrada do usuário não estiver no intervalo especificado, o código exibirá uma caixa de mensagem. Observe o uso do recurso de cadeia de caracteres criado anteriormente para a mensagem de erro.

O exemplo a seguir recupera o nível de efeito da caixa de edição IDC WETMIX e verifica se o valor está dentro de \_ um intervalo especificado:


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



## <a name="storing-the-property-values-in-the-registry"></a>Armazenar os valores de propriedade no Registro

Em seguida, seu código deve persistir os novos valores de propriedade para o Registro. O código a seguir armazena os dois valores de propriedade:


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



## <a name="updating-the-echo-plug-in-property-values"></a>Atualizando os valores de propriedade do plug-in de eco

O **método Apply** deve informar ao plug-in Echo que os valores da propriedade foram alterados. O código a seguir chama o método property put para cada propriedade usando o ponteiro de interface recuperado em CEchoPropPage::SetObjects:


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



Observe que o valor da mistura de umidade é convertido em ponto flutuante antes de ser passado para o plug-in.

## <a name="disabling-the-apply-button"></a>Desabilitando o botão Aplicar

Como etapa final, seu código deve desabilitar Aplicar na caixa de diálogo da página de propriedades como um sinal para o usuário de que os valores foram atualizados com êxito. Isso requer a seguinte linha única de código:


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modificando a página de propriedades de exemplo de eco**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




