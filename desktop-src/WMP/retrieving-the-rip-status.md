---
title: Recuperando o status de resserção
description: Recuperando o status de resserção
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player, CD
- Windows Media Player modelo de objeto, CD
- modelo de objeto, CD
- Windows Media Player ActiveX controle,CD
- ActiveX controle,CD
- Windows Media Player Controle ActiveX dispositivo móvel, CD
- Windows Media Player Móvel, CD
- Cd , recuperando o status do 1000001
- CDs de 1000001, recuperando o status de 1000001
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3210fa9e0db5f9260989d7bebb3650770cec7626892bc20546a6b602fb98955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570187"
---
# <a name="retrieving-the-rip-status"></a>Recuperando o status de resserção

Você pode monitorar o progresso da operação de redução chamando periodicamente [IWMPCdromRip::getripProgress \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Esse método recupera um valor de progresso para toda a operação de responsabilidade. O valor recuperado é um número que representa o percentual de conclusão da recuperação, de 0 a 100.

O valor de progresso representa o percentual concluído de todo o processo de responsabilidade. Para determinar o progresso de uma faixa específica, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) com "RipProgress" como o nome do atributo. Para determinar o índice da faixa que está sendo editada no momento, chame **IWMPPlaylist::getItemInfo** com "CurrentRipTrackIndex" como o nome do atributo.

Você pode monitorar o estado da operação de resserção chamando [periodicamente IWMPCdromRip::getstate \_ ](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Esse método recupera um [valor de enumeração WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica se a operação está em andamento ou interrompida. Você também pode monitorar o estado da operação de manipulação manipulando o evento [IWMPEvents3::CdromRipStateChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) (Consulte [Manipulando eventos em C++.)](handling-events-in-c.md) Tenha cuidado ao comparar o ponteiro **IWMPCdromRip** (fornecido pelo evento) com o ponteiro que representa a operação de resserção, para garantir que o evento tenha sido gerado pela operação.

O código de exemplo a seguir mostra como usar essas funções para recuperar o status de uma operação de ressarção.

Os controles de caixa de diálogo a seguir são definidos para o exemplo de código.



| ID do controle                   | Descrição                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| IDC \_ CURRENT \_ TRACK          | Texto estático que representa o índice da faixa que está sendo desajustada no momento.                                         |
| IDC \_ TRACK \_ PROGRESS \_ TEXT   | Texto estático que representa o progresso da faixa que está sendo ressada como um percentual.                      |
| IDC \_ PROGRESS \_ TRACK         | Barra de progresso com intervalo de 0 a 100 que representa o progresso da faixa que está sendo torcionada atualmente como um percentual. |
| TEXTO DE PROGRESSO \_ \_ GERAL DO IDC \_ | Texto estático que representa o progresso do processo total de ressarção como um percentual.                             |
| PROGRESSO GERAL DO IDC \_ \_       | Barra de progresso com intervalo de 0 a 100 que representa o progresso do processo total de ressarção como um percentual.        |
| ESTADO \_ DE IDC CID \_              | Texto estático que exibe a operação que está sendo executada no momento ("Operação", "Parado" ou "Desconhecido")             |



 


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

[**Ressarça um CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperar a interface de extração**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Iniciando o processo de ressarção**](starting-the-rip-process.md)
</dt> <dt>

[**Selecionando itens para Busca**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




