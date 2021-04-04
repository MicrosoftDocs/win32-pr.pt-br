---
title: Recuperando o status do RIP
description: Recuperando o status do RIP
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, recuperando o status do RIP
- copiando CDs, recuperando o status do RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007152"
---
# <a name="retrieving-the-rip-status"></a>Recuperando o status do RIP

Você pode monitorar o progresso da operação de cópia de CDs chamando periodicamente [IWMPCdromRip:: get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Esse método recupera um valor de progresso para toda a operação de cópia de CDs. O valor recuperado é um número que representa a porcentagem de cópia concluída, de 0 a 100.

O valor de progresso representa a porcentagem completa de todo o processo de cópia de CDs. Para determinar o progresso de uma faixa específica, use [IWMPMedia:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) com "RipProgress" como o nome do atributo. Para determinar o índice da faixa que está sendo copiada no momento, chame **IWMPPlaylist:: getItemInfo** com "CurrentRipTrackIndex" como o nome do atributo.

Você pode monitorar o estado da operação de cópia de CDs chamando periodicamente [IWMPCdromRip:: get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Esse método recupera um valor de enumeração [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica se a operação está em andamento ou foi interrompida. Você também pode monitorar o estado da operação de cópia de CDs manipulando o evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . (Consulte [manipulação de eventos em C++](handling-events-in-c.md).) Tenha cuidado para comparar o ponteiro **IWMPCdromRip** (fornecido pelo evento) com o ponteiro que representa a operação de cópia, a fim de garantir que o evento foi gerado pela operação.

O código de exemplo a seguir mostra como usar essas funções para recuperar o status de uma operação de cópia de CDs.

Os seguintes controles de diálogo são definidos para o exemplo de código.



| ID do controle                   | Description                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| \_faixa atual do IDC \_          | Texto estático que representa o índice da faixa que está sendo copiada no momento.                                         |
| texto de progresso da IDC \_ Track \_ \_   | Texto estático que representa o progresso da faixa atualmente sendo copiada como uma porcentagem.                      |
| \_faixa de progresso da IDC \_         | Barra de progresso com intervalo de 0 a 100 que representa o progresso da faixa que está sendo copiada no momento como uma porcentagem. |
| \_texto de \_ progresso \_ geral da IDC | Texto estático que representa o progresso do processo total de cópia de música como uma porcentagem.                             |
| \_progresso \_ geral da IDC       | Barra de progresso com intervalo de 0 a 100 que representa o progresso do processo total de cópia de música como uma porcentagem.        |
| Estado do IDC \_ RIP \_              | Texto estático que exibe a operação que está sendo executada no momento ("copiando", "parado" ou "desconhecido")             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Copiando um CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperar a interface de extração**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Iniciando o processo de RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Selecionando itens para copiar**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




