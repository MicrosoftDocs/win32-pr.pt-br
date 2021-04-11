---
description: Visão geral da biblioteca COM e notas sobre como usar as seções de tecnologia do Tablet PC do SDK do Windows Vista.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Usando a biblioteca COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82671b198114cf45b334e8c4e07146a91964e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296305"
---
# <a name="using-the-com-library"></a>Usando a biblioteca COM

A referência de biblioteca gerenciada do Tablet PC agora pode ser encontrada na seção referência da biblioteca de classes do SDK do Windows Vista. Ele fornece um modelo de objeto para Microsoft Visual C++. A maioria dos objetos na biblioteca COM são idênticos aos encontrados na API gerenciada do Tablet PC.

No entanto, a API COM contém alguns membros além daqueles encontrados na API gerenciada devido às diferenças entre o ambiente padrão do Microsoft Win32 e o ambiente do SDK do Microsoft .NET (Kit de desenvolvimento do Frameworksoftware). Por exemplo, os objetos InkRectangle e InkTransform são usados em COM, mas o FrameworkSDK fornece implementação nativa para [**classe InkRectangle**](inkrectangle-class.md) e [**classe InkTransform**](inktransform-class.md) que elimina a necessidade desses objetos na API gerenciada da plataforma Tablet PC.

> [!Note]  
> Os objetos na API COM e os controles de tinta não são projetados para uso em páginas de Active Server (ASP).

 

## <a name="working-with-collections"></a>Trabalhando com coleções

Se você passar um valor **nulo** como o índice para qualquer um dos objetos de coleção na biblioteca com, você receberá o primeiro item na coleção porque esses valores de argumento são forçados a 0 quando a chamada é feita.

A propriedade **\_ NewEnum** está marcada como restrita na definição de IDL (linguagem de definição de interface) para as interfaces de coleção.

Em C++, use um `For...` loop para iterar por meio de uma coleção, primeiro obtendo o comprimento da coleção. O exemplo a seguir mostra como iterar os traços de um objeto [**InkDisp**](inkdisp-class.md) , `pInk` .


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

Se você passar o VT \_ vazio ou \_ o VT nulo como o índice para qualquer um dos objetos de coleção na biblioteca com, você receberá o primeiro item na coleção porque esses valores de argumento são forçados a 0 quando a chamada é feita.

## <a name="using-idispatch"></a>Usando IDispatch

Para aumentar o desempenho, a API (interface de programação de aplicativo) COM do Tablet PC Platform não oferece suporte à chamada `IDispatchImpl::Invoke` com uma estrutura DISPPARAMS com argumentos nomeados. O `IDispatchImpl::GetIDsOfNames` também não tem suporte. Em vez disso, chame `Invoke` com os DISPIDs fornecidos nos cabeçalhos do SDK.

## <a name="waiting-for-events"></a>Aguardando eventos

O ambiente do Tablet PC é multithread. Consulte a documentação COM para vários threads.

## <a name="support-for-aggregation"></a>Suporte para agregação

A agregação foi testada apenas para o controle [InkEdit](inkedit-control-reference.md) , o controle [InkPicture](inkpicture-control-reference.md) , o objeto [**InkDisp**](inkdisp-class.md) e o objeto [**InkOverlay**](inkoverlay-class.md) . A agregação não foi testada para outros controles e objetos na biblioteca.

## <a name="c"></a>C++

Usar o SDK do Tablet PC em C++ requer o uso de alguns conceitos COM, como VARIANT, SAFEARRAY e BSTR. Esta seção descreve como usá-los.

### <a name="variant-and-safearray"></a>VARIANTE e SAFEARRAY

A estrutura variante é usada para comunicação entre objetos COM. Essencialmente, a estrutura variante é um contêiner para uma União grande que transporta muitos tipos de dados.

O valor no primeiro membro da estrutura, VT, descreve qual dos membros da União é válido. Ao receber informações em uma estrutura de variante, verifique o membro VT para descobrir qual membro contém dados válidos. Da mesma forma, quando você envia informações usando uma estrutura VARIANT, sempre defina VT para refletir o membro Union que contém as informações.

Antes de usar a estrutura, inicialize-a chamando a função COM VariantInit. Quando terminar com a estrutura, limpe-a antes que a memória que contém a variante seja liberada chamando VariantClear.

Para obter mais informações sobre a estrutura de variante, consulte [tipos de dados Variant e VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

A estrutura SAFEARRAY é fornecida como uma maneira de trabalhar com segurança com matrizes no COM. O campo pArray da variante é um ponteiro para um SAFEARRAY. Use funções como SafeArrayCreateVector, SafeArrayAccessData e SafeArrayUnaccessData para criar e preencher um SAFEARRAY em uma variante.

Para obter mais informações sobre o tipo de dados SAFEARRAY, consulte [tipo de dados SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray).

Este exemplo de C++ cria um [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` , em um objeto [**InkDisp**](inkdisp-class.md) , `pInk` , de uma matriz de dados Point.


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

O formato de cadeia de caracteres com suporte para COM é BSTR. Um BSTR tem um ponteiro para uma cadeia de caracteres terminada em zero, mas também contém o comprimento da cadeia de caracteres (em bytes, não contando o terminador), que é armazenado nos 4 bytes imediatamente antes do primeiro caractere da cadeia de caracteres.

Para obter mais informações sobre BSTR, consulte [tipo de dados BSTR](/previous-versions/windows/desktop/automat/bstr).

Este exemplo de C++ mostra como definir o factor em um [**InkRecognizerContext**](inkrecognizercontext-class.md) usando um BSTR.


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



 

 
