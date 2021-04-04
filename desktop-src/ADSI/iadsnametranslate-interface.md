---
title: Interface IADsNameTranslate
description: A interface IADsNameTranslate é usada para converter nomes distintos entre vários formatos. As traduções de nome são executadas no servidor de diretório, e essa interface está atualmente disponível somente para objetos no Active Directory.
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- ADSI da interface IADsNameTranslate
- IADsTranslate ADSI, usando
- ADSI ADSI, código de exemplo C/C++, usando IADsTranslate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ff5b44288289f118c41463a22e619aa815ecb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822208"
---
# <a name="iadsnametranslate-interface"></a>Interface IADsNameTranslate

A interface [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) é usada para converter nomes distintos entre vários formatos. As traduções de nome são executadas no servidor de diretório, e essa interface está atualmente disponível somente para objetos no Active Directory.

O exemplo de código a seguir converte um nome de conta do formato do Windows em formato LDAP.


```C++
HRESULT TranslateNTNameToLDAPName( BSTR * pNTName, BSTR * pLDAPName )
{
    IADsNameTranslate *pTrans;
    HRESULT hr = S_OK;
 
    hr = CoCreateInstance(CLSID_NameTranslate, 
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsNameTranslate,
                          (void**) &pTrans );
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Init(ADS_NAME_INITTYPE_DOMAIN, 
                      CComBSTR("Fabrikam.com"));
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Set(ADS_NAME_TYPE_NT4, *pNTName);
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Get(ADS_NAME_TYPE_1779, pLDAPName);
    pTrans->Release();
    return hr;
}
```



 

 




