---
description: Visão geral da Biblioteca COM e observações sobre como usar as seções de Tecnologia de Tablet PC do SDK Windows Vista.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Usando a biblioteca COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf986d79011301abe6a9f279a83278fda5dd9e33e3a79335d7d94e6081fb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819136"
---
# <a name="using-the-com-library"></a>Usando a biblioteca COM

A referência da biblioteca gerenciada de tablet pc agora pode ser encontrada na seção de referência Windows biblioteca de classes do SDK do Vista regular. Ele fornece um modelo de objeto para Microsoft Visual C++. A maioria dos objetos na Biblioteca COM é idêntica àquelas encontradas na API Gerenciada de TABLET PC.

No entanto, a API COM contém alguns membros além daqueles encontrados na API Gerenciada devido a diferenças entre o ambiente padrão do Microsoft Win32 e o ambiente do SDK (kit de desenvolvimento de software) do Microsoft .NET Framework. Por exemplo, os objetos InkRectangle e InkTransform são usados em COM, mas o FrameworkSDK fornece implementação nativa para a [**Classe InkRectangle**](inkrectangle-class.md) e a [**Classe InkTransform**](inktransform-class.md) que elimina a necessidade desses objetos na API Gerenciada da plataforma de tablet pc.

> [!Note]  
> Os objetos na API COM e os controles de tinta não são projetados para uso no ASP (Active Server Pages).

 

## <a name="working-with-collections"></a>Trabalhando com coleções

Se você passar um valor **NULL** como o índice para qualquer um dos objetos de coleção na Biblioteca COM, receberá o primeiro item na coleção porque esses valores de argumento são coercados para 0 quando a chamada é feita.

A **\_ propriedade NewEnum** é marcada como restrita na definição de IDL (Interface Definition Language) para as interfaces de coleção.

No C++, use um loop para iterar em uma coleção obtendo primeiro o `For...` comprimento da coleção. O exemplo a seguir mostra como iterar pelos traços de um [**objeto InkDisp,**](inkdisp-class.md) `pInk` .


```C++
IInkStrokes* pStrokes;
HRESULT result = pInk->get_Strokes(&pStrokes);
if (SUCCEEDED(result))
{
    // Loop over strokes
    long nStrokes;
    result = pStrokes->get_Count(&nStrokes);
    if (SUCCEEDED(result))
    {
        for (int i =0; i < nStrokes; i++)
        {
            IInkStrokeDisp* pStroke;
            result = pStrokes->Item(i, &pStroke);
            if (SUCCEEDED(result))
            {
              // Code that uses pStroke
              // ...
            }
        }
    }
}
```



## <a name="parameters"></a>Parâmetros

Se você passar VT EMPTY ou VT NULL como o índice para qualquer um dos objetos de coleção na Biblioteca COM, receberá o primeiro item na coleção porque esses valores de argumento são \_ coercados para 0 quando a chamada \_ é feita.

## <a name="using-idispatch"></a>Usando IDispatch

Para aumentar o desempenho, a API (interface de programação de aplicativo) COM da Plataforma de Tablet PC não dá suporte à chamada com uma estrutura `IDispatchImpl::Invoke` DISPPARAMS com argumentos nomeados. Também `IDispatchImpl::GetIDsOfNames` não há suporte para o . Em vez disso, `Invoke` chame com os DISPIDs fornecidos nos headers do SDK.

## <a name="waiting-for-events"></a>Aguardando eventos

O ambiente do tablet pc é multithreaded. Consulte a documentação COM para multi-threading.

## <a name="support-for-aggregation"></a>Suporte para agregação

A agregação foi testada apenas para o controle [InkEdit,](inkedit-control-reference.md) o controle [InkPicture,](inkpicture-control-reference.md) o objeto [**InkDisp**](inkdisp-class.md) e o [**objeto InkOverlay.**](inkoverlay-class.md) A agregação não foi testada para outros controles e objetos na biblioteca.

## <a name="c"></a>C++

Usar o SDK do Tablet PC em C++ requer o uso de alguns conceitos COM, como VARIANT, SAFEARRAY e BSTR. Esta seção descreve como usá-los.

### <a name="variant-and-safearray"></a>VARIANT e SAFEARRAY

A estrutura VARIANT é usada para comunicação entre objetos COM. Essencialmente, a estrutura VARIANT é um contêiner para uma grande união que carrega muitos tipos de dados.

O valor no primeiro membro da estrutura, vt, descreve qual dos membros da união é válido. Quando você receber informações em uma estrutura VARIANT, verifique o membro vt para descobrir qual membro contém dados válidos. Da mesma forma, quando você envia informações usando uma estrutura VARIANT, sempre de definido vt para refletir o membro da união que contém as informações.

Antes de usar a estrutura , inicialize-a chamando a função VARIANTInit COM. Quando terminar com a estrutura, limpe-a antes que a memória que contém a VARIANT seja liberada chamando VariantClear.

Para obter mais informações sobre a estrutura VARIANT, consulte [TIPOS de dados VARIANT e VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

A estrutura SAFEARRAY é fornecida como uma maneira de trabalhar com segurança com matrizes em COM. O campo de análise variant é um ponteiro para um SAFEARRAY. Use funções como SafeArrayCreateVector, SafeArrayAccessData e SafeArrayUnaccessData para criar e preencher um SAFEARRAY em uma VARIANT.

Para obter mais informações sobre o tipo de dados SAFEARRAY, consulte [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).

Este exemplo de C++ cria [**um IInkStrkeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , , em um objeto `pInkStrokeDisp` [**InkDisp,**](inkdisp-class.md) `pInk` , de uma matriz de dados de ponto.


```C++
VARIANT   var, varPK;
LONG*   plongArray=NULL;
POINT   ptArray[2]={0};
long   lSize=0;
IInkStrokeDisp* pInkStrokeDisp;

IInkDisp*   pInk;   // the object should be created correctly 
                    // elsewhere and assigned here.
HRESULT   hr=E_FAIL;

ptArray[0].x = 20;
ptArray[0].y = 100;
ptArray[1].x = 30;
ptArray[1].y = 110;
lSize = 2;   // two points

VariantInit( &var );
VariantInit( &varPK );
SAFEARRAY* psa = SafeArrayCreateVector( VT_I4, 0, lSize*2 );
if( psa )
{
  if( SUCCEEDED( hr = SafeArrayAccessData( psa, (void**)&plongArray) ))
   {
      for( long i = 0; i < lSize; i++ ) 
      {
         plongArray[2*i] = ptArray[i].x;
         plongArray[2*i+1] = ptArray[i].y;
      }
      hr = SafeArrayUnaccessData( psa );

      if ( SUCCEEDED( hr ) ) 
      {
         var.vt     = VT_ARRAY | VT_I4;
         var.parray = psa;

        // varPK (packet description) is currently reserved, so it is
        // just empty variant for now.
         pInk->CreateStroke( var, varPK, &pInkStrokeDisp );   
      }
   }
}
VariantClear( &var );
VariantClear( &varPK );
```



### <a name="bstr"></a>BSTR

O formato de cadeia de caracteres com suporte para COM é BSTR. Uma BSTR tem um ponteiro para uma cadeia de caracteres terminada em zero, mas também contém o comprimento da cadeia de caracteres (em bytes, sem contar o terminador), que é armazenado nos 4 bytes imediatamente anteriores ao primeiro caractere da cadeia de caracteres.

Para obter mais informações sobre BSTR, consulte [Tipo de dados BSTR](/previous-versions/windows/desktop/automat/bstr).

Este exemplo de C++ mostra como definir o factoid em [**um InkRecognizerContext**](inkrecognizercontext-class.md) usando um BSTR.


```C++
IInkRecognizerContext* pRecognizerContext = NULL;
result = CoCreateInstance(CLSID_InkRecognizerContext, 
    NULL, CLSCTX_INPROC_SERVER,
    IID_IInkRecognizerContext, 
    (void **) &pRecognizerContext);
if SUCCEEDED(result)
{
    BSTR bstrFactoid = SysAllocString(FACTOID_DATE);
    result = pRecognizerContext->put_Factoid(bstrFactoid);
    if SUCCEEDED(result)
    {
      // Use recognizer context...
      // ...
    }
    SysFreeString(bstrFactoid);
}
```



 

 
