---
title: Extrair usando IWMPPlayerServices setTaskPane
description: Extrair usando IWMPPlayerServices setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player, CD de cds
- modelo de objeto Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- controle de ActiveX de Windows Media Player, CD de cds
- controle de ActiveX, CD de cds
- Windows Media Player controle de ActiveX móvel, CD de cds
- Windows Media Player Dispositivos móveis e de CDs
- CD de CDs, IWMPPlayerServices setTaskPane interface
- copiando CDs, IWMPPlayerServices setTaskPane interface
- Interface IWMPPlayerServices setTaskPane
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2abf53d29284b5da629598e6f23d6dcae78c69c60c23ba07f30445d5252845e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569829"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Copiando por meio de IWMPPlayerServices:: setTaskPane

> [!Note]  
> esta seção documenta um recurso dos controles Windows Media Player 9 Series e Windows Media Player 10 ActiveX. É recomendável que você use a interface **IWMPCdromRip** com versões posteriores. Consulte a [interface IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).

 

você pode usar o controle Windows Media Player 9 Series ou posterior para copiar as faixas de CD para o computador do usuário. Esse processo é chamado de *cópia de CDs*. para fazer isso, você deve inserir o controle de Windows Media Player no modo remoto. para obter mais informações sobre o modo remoto, consulte [comunicação remota do controle de Windows Media Player](remoting-the-windows-media-player-control.md).

Para iniciar o processo de cópia de CDs, chame [IWMPPlayerServices:: setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passando o CopyFromCD? Autocopie: o valor de *ID* para o parâmetro *bstrTaskPane* , em que *ID* é o índice da unidade de CD da qual copiar. Esse índice corresponde ao índice de um objeto de **cdrom** na interface **IWMPCdromCollection** ou ao evento **CdromMediaChange** .

O código de exemplo a seguir é uma função que inicia o processo de copiar um CD da unidade de CD identificada pelo índice zero. A função usa a seguinte variável de membro:


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



O código a seguir mostra o corpo da função:


```C++
HRESULT CMyApp::StartRip()
{
    CComPtr<IWMPPlayerApplication>  spPlayerApp;
    CComPtr<IWMPPlayerServices>     spPlayerServices;
    CComBSTR bstrParam;  // Contains the parameter string.

    ATLASSERT(m_spPlayer.p);

    HRESULT hr = m_spPlayer->QueryInterface(&spPlayerServices);

    if(SUCCEEDED(hr))
    {
        // Create the parameter string.
        hr = bstrParam.Append(_T("CopyFromCD?AutoCopy:0"));
    }

    if(SUCCEEDED(hr))
    {
        // Rip the CD in drive 0.
        hr = spPlayerServices->setTaskPane(bstrParam);
    }

    return hr;
}

```



Exibindo o status para o usuário

Ao copiar de um CD, você pode recuperar uma cadeia de caracteres que contém informações de status sobre a operação de cópia. Para fazer isso, primeiro você deve recuperar uma lista de reprodução que contém itens de mídia que representam as faixas do CD chamando [IWMPCdrom:: get \_ playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist). Como no exemplo anterior, o código de exemplo a seguir funciona com o índice de unidade de CD zero. Ele armazena a lista de reprodução recuperada na seguinte variável de membro:


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



O código a seguir mostra o corpo da função:


```C++
HRESULT CMyApp::GetCDPlaylist()
{
    HRESULT hr = S_OK;

    // Release any existing playlist instance.
    m_spCDPlaylist.Release();

    CComPtr<IWMPCdromCollection> spCDDrives;
    CComPtr<IWMPCdrom>  spDrive;
    long lCount = 0;  // Count of CD drives.

    ATLASSERT(m_spPlayer);

    hr = m_spPlayer->get_cdromCollection(&spCDDrives);

    // Test to make sure there is at least one drive.
    if(SUCCEEDED(hr))
    {
        hr = spCDDrives->get_count(&lCount);
    }

    if(SUCCEEDED(hr) && lCount < 1)
    {
        MessageBox(_T("No CD drive detected"), 
                   _T("CD Rip Error"), MB_OK);
        hr = NS_E_CD_READ_ERROR;
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the first drive.
        hr = spCDDrives->item(0, &spDrive);
    }
    
    if(SUCCEEDED(hr))
    {
        // Get the playlist.
        hr = spDrive->get_playlist(&m_spCDPlaylist);
    }
   
    return hr;
}

```



Em seguida, manipule o evento [IWMPEvents:: MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) . Esse evento ocorre quando uma faixa de CD está sendo copiada. O ponteiro **IDispatch** passado para o manipulador de eventos aponta para a interface **IWMPMedia** para a faixa do CD. Chame **QueryInterface** por meio de **IDispatch** para recuperar o ponteiro para **IWMPMedia**.

Para detectar qual faixa de CD está sendo copiada, compare o ponteiro **IWMPMedia** do evento com os itens de mídia na lista de reprodução de CD chamando [IWMPMedia:: get \_ isidêntico](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).

Chame [IWMPMedia:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passando a cadeia de caracteres "status" como o nome do item. **Status** é um atributo temporário definido por Windows Media Player em itens de mídia enquanto eles estão sendo copiados do CD; Ele não está disponível na biblioteca do.

O código de exemplo a seguir mostra um manipulador de eventos **MediaChange** .


```C++
void CMyApp::MediaChange(IDispatch * Item)
{
    // Test whether the CD playlist exists.
    if(!m_spCDPlaylist)
    {
        return;
    }

    // Declare and initialize variables.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = S_OK;
    VARIANT_BOOL vbIdentical = VARIANT_FALSE;
    CComBSTR bstrVal;
    CComBSTR bstrName;
    long lCount = 0;  

    // Create the attribute value string.
    hr = bstrName.Append(_T("Status"));

    if(SUCCEEDED(hr))
    { 
        // Retrieve the IWMPMedia pointer from IDispatch.
        hr = Item->QueryInterface(__uuidof(IWMPMedia),(void**)&spMedia);
    }

    if(SUCCEEDED(hr))
    {
        // Get the value of the Status attribute.
        hr = spMedia->getItemInfo(bstrName, &bstrVal);
    }

    if(SUCCEEDED(hr))
    {
        // If the attribute is empty, set a failure code
        // to simply exit the function.
        if(bstrVal.Length() == 0)
        {
            hr = E_PENDING;
        }
    }
      
    if(SUCCEEDED(hr))
    {
        // Retrieve the count of items in the CD playlist.
        hr = m_spCDPlaylist->get_count(&lCount);
    }

    if(lCount < 1)
    {
        // Exit if the playlist is empty.
        hr = E_PENDING;
    }    

    if(SUCCEEDED(hr) && spMedia)
    {
        // Iterate through the playlist.
        // Compare the media item that raised the event
        // to each CD track. This detects which track
        // has a new status.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spTrack;

            // Retrieve the CD track as a media object.
            hr = m_spCDPlaylist->get_item(i, &spTrack);

            if(SUCCEEDED(hr))
            {
                // Do the comparison.
                hr = spMedia->get_isIdentical(spTrack, &vbIdentical);
            }

            if(SUCCEEDED(hr) && VARIANT_TRUE == vbIdentical)
            {
                 // spTrack represents a track with changed status.
                 // bstrVal contains a status string. For example:
                 // "Ripping (10%)"
                 //
                 // TODO: Retrieve metadata about the track, and then
                 // display the status to the user.
            }
        }
    }

    return;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMPCdrom**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interface IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Interface IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[**Interface IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interface IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[**Interface IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Guia de controle do Player**](player-control-guide.md)
</dt> <dt>

[**Copiando usando a interface IWMPCdromRip**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




