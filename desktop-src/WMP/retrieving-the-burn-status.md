---
title: Recuperando o status da gravação
description: Recuperando o status da gravação
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, recuperando status de gravação
- gravando CDs, recuperando o status da gravação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103917007"
---
# <a name="retrieving-the-burn-status"></a>Recuperando o status da gravação

No exemplo de código a seguir, os seguintes controles de diálogo são definidos:



| ID do controle           | Description                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| \_estado de gravação do IDC \_     | Texto estático que representa o estado da operação de gravação de CD.             |
| progresso da IDC \_        | Barra de progresso com um intervalo de 0 a 100 que representa o progresso total de gravação. |
| \_texto de progresso da IDC \_  | Texto estático que representa o progresso total da gravação como um número de 0 a 100. |
| \_hora disponível do IDC \_ | Texto estático para exibir o tempo disponível no CD, em segundos.               |
| \_espaço livre da IDC \_     | Texto estático para exibir o espaço livre no CD, em bytes.                     |
| \_espaço total da IDC \_    | Texto estático para exibir a capacidade total do CD, em bytes.                 |



 

Você pode monitorar o progresso da operação de gravação chamando periodicamente [IWMPCdromBurn:: get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) enquanto o CD está sendo gravado. Esse método recupera um valor de progresso para toda a operação de gravação. O valor recuperado é um número que representa a porcentagem de gravação concluída, de 0 a 100.


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



Você pode obter o estado atual da operação de gravação chamando [IWMPCdromBurn:: get \_ gravástate](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate). Esse método recupera uma enumeração que especifica a operação atual que está sendo executada.


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



Para recuperar o número de segundos de áudio que o CD pode conter, chame [IWMPCdromBurn:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) com "availabletime" como o primeiro parâmetro. O valor recuperado por essa função é representado por uma cadeia de caracteres.


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



Para recuperar a quantidade de espaço livre em um disco, chame **IWMPCdromBurn:: getItemInfo** com "Freespace" como o primeiro parâmetro. O valor recuperado por essa função é uma cadeia de caracteres que representa o número de bytes livres disponíveis no disco.


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



Para recuperar a capacidade total de um disco, chame **IWMPCdromBurn:: getItemInfo** com "TotalSpace" como o primeiro parâmetro. O valor recuperado por essa função é uma cadeia de caracteres que corresponde ao número total de bytes no disco.


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando um CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperar a interface de gravação de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Iniciando o processo de gravação**](starting-the-burn-process.md)
</dt> <dt>

[**Apagando um CD regravável**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperando a unidade e o status do disco**](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




