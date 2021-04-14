---
title: Extrair usando IWMPPlayerServices setTaskPane
description: Extrair usando IWMPPlayerServices setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, IWMPPlayerServices setTaskPane interface
- copiando CDs, IWMPPlayerServices setTaskPane interface
- Interface IWMPPlayerServices setTaskPane
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104453881"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a><span data-ttu-id="95e04-113">Copiando por meio de IWMPPlayerServices:: setTaskPane</span><span class="sxs-lookup"><span data-stu-id="95e04-113">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="95e04-114">Esta seção documenta um recurso dos controles ActiveX do Windows Media Player 9 Series e do Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="95e04-114">This section documents a feature of the Windows Media Player 9 Series and Windows Media Player 10 ActiveX controls.</span></span> <span data-ttu-id="95e04-115">É recomendável que você use a interface **IWMPCdromRip** com versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="95e04-115">It is recommended that you use the **IWMPCdromRip** interface with later versions.</span></span> <span data-ttu-id="95e04-116">Consulte a [interface IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span><span class="sxs-lookup"><span data-stu-id="95e04-116">See [IWMPCdromRip Interface](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span></span>

 

<span data-ttu-id="95e04-117">Você pode usar o controle Windows Media Player 9 Series ou posterior para copiar faixas de CD para o computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="95e04-117">You can use the Windows Media Player 9 Series or later control to copy CD tracks to the user's computer.</span></span> <span data-ttu-id="95e04-118">Esse processo é chamado de *cópia de CDs*.</span><span class="sxs-lookup"><span data-stu-id="95e04-118">This process is called *ripping*.</span></span> <span data-ttu-id="95e04-119">Para fazer isso, você deve inserir o controle do Windows Media Player no modo remoto.</span><span class="sxs-lookup"><span data-stu-id="95e04-119">To do this, you must embed the Windows Media Player control in remote mode.</span></span> <span data-ttu-id="95e04-120">Para obter mais informações sobre o modo remoto, consulte [comunicação remota do controle do Windows Media Player](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="95e04-120">For more information about remote mode, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

<span data-ttu-id="95e04-121">Para iniciar o processo de cópia de CDs, chame [IWMPPlayerServices:: setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passando o CopyFromCD? Autocopie: o valor de *ID* para o parâmetro *bstrTaskPane* , em que *ID* é o índice da unidade de CD da qual copiar.</span><span class="sxs-lookup"><span data-stu-id="95e04-121">To start the ripping process, call [IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passing the CopyFromCD?AutoCopy:*id* value for the *bstrTaskPane* parameter, where *id* is the index of the CD drive from which to copy.</span></span> <span data-ttu-id="95e04-122">Esse índice corresponde ao índice de um objeto de **cdrom** na interface **IWMPCdromCollection** ou ao evento **CdromMediaChange** .</span><span class="sxs-lookup"><span data-stu-id="95e04-122">This index corresponds to the index of a **Cdrom** object in the **IWMPCdromCollection** interface or the **CdromMediaChange** event.</span></span>

<span data-ttu-id="95e04-123">O código de exemplo a seguir é uma função que inicia o processo de copiar um CD da unidade de CD identificada pelo índice zero.</span><span class="sxs-lookup"><span data-stu-id="95e04-123">The following example code is a function that starts the process of ripping a CD from the CD drive identified by index zero.</span></span> <span data-ttu-id="95e04-124">A função usa a seguinte variável de membro:</span><span class="sxs-lookup"><span data-stu-id="95e04-124">The function uses the following member variable:</span></span>


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



<span data-ttu-id="95e04-125">O código a seguir mostra o corpo da função:</span><span class="sxs-lookup"><span data-stu-id="95e04-125">The following code shows the body of the function:</span></span>


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



<span data-ttu-id="95e04-126">Exibindo o status para o usuário</span><span class="sxs-lookup"><span data-stu-id="95e04-126">Displaying Status to the User</span></span>

<span data-ttu-id="95e04-127">Ao copiar de um CD, você pode recuperar uma cadeia de caracteres que contém informações de status sobre a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="95e04-127">When copying from a CD, you can retrieve a string containing status information about the copy operation.</span></span> <span data-ttu-id="95e04-128">Para fazer isso, primeiro você deve recuperar uma lista de reprodução que contém itens de mídia que representam as faixas do CD chamando [IWMPCdrom:: get \_ playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span><span class="sxs-lookup"><span data-stu-id="95e04-128">To do this, you must first retrieve a playlist containing media items that represent the CD tracks by calling [IWMPCdrom::get\_playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span></span> <span data-ttu-id="95e04-129">Como no exemplo anterior, o código de exemplo a seguir funciona com o índice de unidade de CD zero.</span><span class="sxs-lookup"><span data-stu-id="95e04-129">Like the previous example, the following example code works with CD drive index zero.</span></span> <span data-ttu-id="95e04-130">Ele armazena a lista de reprodução recuperada na seguinte variável de membro:</span><span class="sxs-lookup"><span data-stu-id="95e04-130">It stores the retrieved playlist in the following member variable:</span></span>


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



<span data-ttu-id="95e04-131">O código a seguir mostra o corpo da função:</span><span class="sxs-lookup"><span data-stu-id="95e04-131">The following code shows the body of the function:</span></span>


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



<span data-ttu-id="95e04-132">Em seguida, manipule o evento [IWMPEvents:: MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) .</span><span class="sxs-lookup"><span data-stu-id="95e04-132">Next, handle the [IWMPEvents::MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) event.</span></span> <span data-ttu-id="95e04-133">Esse evento ocorre quando uma faixa de CD está sendo copiada.</span><span class="sxs-lookup"><span data-stu-id="95e04-133">This event occurs when a CD track is being ripped.</span></span> <span data-ttu-id="95e04-134">O ponteiro **IDispatch** passado para o manipulador de eventos aponta para a interface **IWMPMedia** para a faixa do CD. Chame **QueryInterface** por meio de **IDispatch** para recuperar o ponteiro para **IWMPMedia**.</span><span class="sxs-lookup"><span data-stu-id="95e04-134">The **IDispatch** pointer passed to the event handler points to the **IWMPMedia** interface for the CD track. Call **QueryInterface** through **IDispatch** to retrieve the pointer to **IWMPMedia**.</span></span>

<span data-ttu-id="95e04-135">Para detectar qual faixa de CD está sendo copiada, compare o ponteiro **IWMPMedia** do evento com os itens de mídia na lista de reprodução de CD chamando [IWMPMedia:: get \_ isidêntico](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span><span class="sxs-lookup"><span data-stu-id="95e04-135">To detect which CD track is being ripped, compare the **IWMPMedia** pointer from the event to the media items in the CD playlist by calling [IWMPMedia::get\_isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span></span>

<span data-ttu-id="95e04-136">Chame [IWMPMedia:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passando a cadeia de caracteres "status" como o nome do item.</span><span class="sxs-lookup"><span data-stu-id="95e04-136">Call [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passing the string "Status" as the item name.</span></span> <span data-ttu-id="95e04-137">**Status** é um atributo temporário definido pelo Windows Media Player em itens de mídia enquanto eles estão sendo copiados do CD; Ele não está disponível na biblioteca do.</span><span class="sxs-lookup"><span data-stu-id="95e04-137">**Status** is a temporary attribute set by Windows Media Player on media items while they are being ripped from CD; it is not available from the library.</span></span>

<span data-ttu-id="95e04-138">O código de exemplo a seguir mostra um manipulador de eventos **MediaChange** .</span><span class="sxs-lookup"><span data-stu-id="95e04-138">The following example code shows a **MediaChange** event handler.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="95e04-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95e04-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95e04-140">**Interface IWMPCdrom**</span><span class="sxs-lookup"><span data-stu-id="95e04-140">**IWMPCdrom Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[<span data-ttu-id="95e04-141">**Interface IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="95e04-141">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[<span data-ttu-id="95e04-142">**Interface IWMPEvents**</span><span class="sxs-lookup"><span data-stu-id="95e04-142">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[<span data-ttu-id="95e04-143">**Interface IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="95e04-143">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="95e04-144">**Interface IWMPPlayerServices**</span><span class="sxs-lookup"><span data-stu-id="95e04-144">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[<span data-ttu-id="95e04-145">**Interface IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="95e04-145">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="95e04-146">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="95e04-146">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> <dt>

[<span data-ttu-id="95e04-147">**Copiando usando a interface IWMPCdromRip**</span><span class="sxs-lookup"><span data-stu-id="95e04-147">**Ripping by Using the IWMPCdromRip Interface**</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




