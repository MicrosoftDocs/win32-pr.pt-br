---
title: Funções auxiliares de enumeração
description: Há três funções auxiliares de enumerador que podem ser usadas do C/C++ para auxiliar na navegação de objetos de Active Directory. Eles são ADsBuildEnumerator, ADsEnumerateNext e ADsFreeEnumerator.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- ADsBuildEnumerator ADSI, usando
- ADsEnumerateNext ADSI, usando
- ADsFreeEnumerator ADSI, usando
- ADSI ADSI, código de exemplo C/C++, usando ADsBuildEnumerator ADsEnumerateNext e ADsFreeEnumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c110fbc4fddd420bf8205d6c2d894c7d4f4daf8287312c2d0d86002f5520310b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082650"
---
# <a name="enumeration-helper-functions"></a>Funções auxiliares de enumeração

Há três funções auxiliares de enumerador que podem ser usadas do C/C++ para auxiliar na navegação de objetos de Active Directory. Eles são [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)e [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).

## <a name="adsbuildenumerator"></a>ADsBuildEnumerator

A função auxiliar [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) encapsula o código necessário para criar um objeto enumerador. Ele chama o método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) para criar um objeto enumerador e, em seguida, chama o método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para obter um ponteiro para a interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) para esse objeto. O objeto de enumeração é o mecanismo de automação a ser enumerado em contêineres. Use a função [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) para liberar este objeto do enumerador.

## <a name="adsenumeratenext"></a>ADsEnumerateNext

A função auxiliar [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) popula uma matriz variante com elementos buscados de um objeto enumerador. O número de elementos recuperados pode ser menor do que o número solicitado.

## <a name="adsfreeenumerator"></a>ADsFreeEnumerator

Libera um objeto Enumerator criado anteriormente por meio da função [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) .

O exemplo de código a seguir mostra uma função que usa funções auxiliares de enumerador em C++.


```C++
/*****************************************************************************
  Function:    TestEnumObject
  Arguments:   pszADsPath - ADsPath of the container to be enumerated (WCHAR*).
  Return:      S_OK if successful, an error code otherwise.
  Purpose:     Example using ADsBuildEnumerator, ADsEnumerateNext and
               ADsFreeEnumerator.
******************************************************************************/
#define MAX_ENUM      100  
 
HRESULT
TestEnumObject( LPWSTR pszADsPath )
{
    ULONG cElementFetched = 0L;
    IEnumVARIANT * pEnumVariant = NULL;
    VARIANT VariantArray[MAX_ENUM];
    HRESULT hr = S_OK;
    IADsContainer * pADsContainer =  NULL;
    DWORD dwObjects = 0, dwEnumCount = 0, i = 0;
    BOOL  fContinue = TRUE;
 
 
    hr = ADsGetObject(
                pszADsPath,
                IID_IADsContainer,
                (void **)&pADsContainer
                );
 
 
    if (FAILED(hr)) {
 
        printf("\"%S\" is not a valid container object.\n", pszADsPath) ;
        goto exitpoint ;
    }
 
    hr = ADsBuildEnumerator(
            pADsContainer,
            &pEnumVariant
            );
 
    if( FAILED( hr ) )
    {
      printf("ADsBuildEnumerator failed with %lx\n", hr ) ;
      goto exitpoint ;
    }
 
    fContinue  = TRUE;
    while (fContinue) {
 
        IADs *pObject ;
 
        hr = ADsEnumerateNext(
                    pEnumVariant,
                    MAX_ENUM,
                    VariantArray,
                    &cElementFetched
                    );

        if ( FAILED( hr ) )
        {
            printf("ADsEnumerateNext failed with %lx\n",hr);
            goto exitpoint;
        }
 
        if (hr == S_FALSE) {
            fContinue = FALSE;
        }
 
        dwEnumCount++;
 
        for (i = 0; i < cElementFetched; i++ ) {
 
            IDispatch *pDispatch    = NULL;
            BSTR        bstrADsPath = NULL;
 
            pDispatch = VariantArray[i].pdispVal;
 
            hr = V_DISPATCH( VariantArray + i )->QueryInterface(IID_IADs, (void **) &pObject) ;
 
            if( SUCCEEDED( hr ) )
            {
               pObject->get_ADsPath( &bstrADsPath );
               printf( "%S\n", bstrADsPath );
            }
            pObject->Release();
            VariantClear( VariantArray + i );
            SysFreeString( bstrADsPath );
        }
 
        dwObjects += cElementFetched;
    }
 
    printf("Total Number of Objects enumerated is %d\n", dwObjects);
 
exitpoint:
    if (pEnumVariant) {
        ADsFreeEnumerator( pEnumVariant );
    }
 
    if (pADsContainer) {
        pADsContainer->Release();
    }
 
    return(hr);
}
```



 

 