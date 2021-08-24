---
description: Implementação de conversão de um objeto de tinta de texto (tInk) para tinta.
ms.assetid: 9365da4c-3667-49f0-838f-f099d28dab44
title: Convertendo um objeto de tinta de texto em tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef543fda3ed53123e99ee042aed67af9cedfef3533ae47bc40d8dd284a73675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941156"
---
# <a name="converting-a-text-ink-object-to-ink"></a>Convertendo um objeto de tinta de texto em tinta

Implementação de conversão de um objeto de tinta de texto (tInk) para tinta.

## <a name="to-convert-from-a-text-ink-object-to-ink"></a>Para converter de um objeto de tinta de texto em tinta

1.  Use a interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para gravar o conteúdo do objeto de tinta de texto em um fluxo. O objeto de tinta de texto usa o formato serializado da tinta para gravar no fluxo.
2.  Leia o conteúdo do fluxo em uma matriz de bytes.
3.  Use o método [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) do objeto [**InkDisp**](inkdisp-class.md) para carregar o conteúdo do fluxo no objeto **InkDisp** .

## <a name="text-ink-object-to-ink-object-example"></a>Exemplo de objeto de tinta de texto para objeto de tinta

O fragmento de código a seguir converte um objeto de tinta de texto em tinta.

Primeiro, o código obtém um objeto de tinta de texto.


```C++
/* Create a variable to hold the text ink object */
CComPtr<IInkObject *> spITextInk;

/* Obtain the text ink object */
```



Em seguida, o código cria um ponteiro para o fluxo que contém o conteúdo do objeto de tinta de texto.


```C++
// Create a Stream pointer to hold the saved object
CComPtr<IStream *> spStream = NULL; 
```



Em seguida, o código obtém a interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) do objeto de tinta de texto.


```C++
// Declare the IPersistStream to be used for retrieving the saved data from the text ink
CComPtr<IPersistStream *> spIPersistStream = NULL;
// Get the actual IPersistStream interface off of the TextInk
HRESULT hr = pITextInk->QueryInterface(IID_IPersistStream, (void **)&spIPersistStream);
ASSERT(SUCCEEDED(hr) && spIPersistStream);
```



Em seguida, o código usa a interface [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para salvar o conteúdo do objeto de tinta de texto no fluxo.


```C++
if( SUCCEEDED(hr) && pIPersistStream )
{
    // Create the stream 
    if( SUCCEEDED(hr=CreateStreamOnHGlobal(NULL, TRUE, &spStream)) && spStream )
    {
        // Save the TextInk through IPersistStream Interface to the IStream
        hr = spIPersistStream->Save(spStream, FALSE);
    }
}
```



Em seguida, o código cria um objeto [**InkCollector**](inkcollector-class.md) , cria um objeto [**InkDisp**](inkdisp-class.md) para o **InkCollector**, anexa o **InkCollector** à janela do aplicativo e habilita a coleta de tinta no **InkCollector**.


```C++
// Now create an InkCollector object along with InkDisp Object
if( SUCCEEDED(hr) && spStream)
{
    CComPtr<IInkCollector *> spIInkCollector;
    CComPtr<IInkDisp *> spIInkDisp = NULL;

    // Create the InkCollector object.
    hr = CoCreateInstance(CLSID_InkCollector, 
        NULL, CLSCTX_INPROC_SERVER, 
        IID_IInkCollector, 
        (void **) &spIInkCollector);
    if (FAILED(hr)) 
        return -1;

    // Get a pointer to the Ink object
    hr = spIInkCollector->get_Ink(&spIInkDisp);
    if (FAILED(hr)) 
        return -1;

    // Tell InkCollector the window to collect ink in
    hr = spIInkCollector->put_hWnd((long)hwnd);
    if (FAILED(hr)) 
        return -1;

    // Enable ink input in the window
    hr = spIInkCollector->put_Enabled(VARIANT_TRUE);
    if (FAILED(hr)) 
        return -1;
```



Em seguida, o código recupera o tamanho do fluxo e cria uma matriz segura para manter o conteúdo do fluxo.


```C++
    // Now create a variant data type based on the IStream data
    const LARGE_INTEGER li0 = {0, 0};
    ULARGE_INTEGER uli = {0,0};

    // Find the size of the stream
    hr = spStream->Seek(li0, STREAM_SEEK_END, &uli);
    ASSERT(0 == uli.HighPart);
    DWORD dwSize = uli.LowPart;

    // Set uli to point to the beginning of the stream.
    hr=spStream->Seek(li0, STREAM_SEEK_SET, &uli);
    ASSERT(SUCCEEDED(hr));

    // Create a safe array to hold the stream contents
    if( SUCCEEDED(hr) )
    {
        VARIANT vtData;
        VariantInit(&vtData);
        vtData.vt = VT_ARRAY | VT_UI1;

        vtData.parray = ::SafeArrayCreateVector(VT_UI1, 0, dwSize);
        if (vtData.parray)
        {
```



Por fim, o código acessa a matriz segura e usa o método [**Load**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load) do objeto [**InkDisp**](inkdisp-class.md) para carregar a tinta da matriz.


```C++
            DWORD dwRead = 0;
            LPBYTE pbData = NULL; 

            if (SUCCEEDED(::SafeArrayAccessData(vtData.parray, (void**)&pbData)))
            {
                // Read the data from the stream to the varian data and load that into an InkDisp object
                if (TRUE == spStream->Read(pbData, uli.LowPart, &dwRead)
                    && SUCCEEDED(spIInkDisp->Load(vtData)))
                {
                    hr = S_OK;
                }
                ::SafeArrayUnaccessData(vtData.parray);
            }
            ::SafeArrayDestroy(vtData.parray);
        }
    }
}
```



 

 
