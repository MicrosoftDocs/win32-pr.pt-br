---
description: O controle de registro de certificado instanciado em C++
ms.assetid: 19dd2fce-b4a9-44fd-9572-897ee7943914
title: O controle de registro de certificado instanciado em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935d40c7b4fc041522a0710220addf89b523b3bc6301e7371e5f9bcd541725d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972050"
---
# <a name="the-certificate-enrollment-control-instantiated-in-c"></a>O controle de registro de certificado instanciado em C++

O exemplo de C++ a seguir inicializa COM, cria uma instância do [controle de registro de certificado](certificate-enrollment-control.md), usa o controle de registro de certificado e libera recursos.

## <a name="example-in-c"></a>Exemplo em C++

O exemplo a seguir cria uma instância do [controle de registro de certificado](certificate-enrollment-control.md) e exibe o valor da propriedade [**mystorename**](/windows/win32/api/xenroll/nf-xenroll-icenroll-get_mystorename) . Este exemplo usa a interface [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) .


```C++
#include <windows.h>
#include <stdio.h>
#include <xenroll.h>

// Copyright (C) Microsoft.  All rights reserved.
HRESULT __cdecl main(void)
{
    HRESULT hr = 0;
    ICEnroll4 *pEnroll = NULL;
    BSTR bstrStoreName = NULL;

    // Initialize COM.
    hr = CoInitializeEx( NULL, COINIT_APARTMENTTHREADED );
    if ( FAILED( hr ) )
    {
        printf("Failed CoInitializeEx - [0x%x]\n", hr);
        exit(hr);
    }

    // Create an instance of the object.
    hr = CoCreateInstance( __uuidof(CEnroll),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(ICEnroll4),
                           (void **)&pEnroll);
    if ( FAILED( hr ) )
    {
        printf("Failed CoCreateInstance - pEnroll [0x%x]\n", hr);
        exit(hr);
    }

    hr = pEnroll->get_MyStoreName(&bstrStoreName);
    if (SUCCEEDED(hr))
    {
        printf("The value of MyStoreName is %ws\n", bstrStoreName);
    }
    else
    {
        printf("pEnroll->GetMyStoreName failed: 0x%x\n", hr);
    }

    pEnroll->Release();
    SysFreeString(bstrStoreName);
    CoUninitialize();

    return hr;
}
```



 

 
