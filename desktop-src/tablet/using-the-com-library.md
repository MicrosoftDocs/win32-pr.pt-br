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
# <a name="using-the-com-library"></a><span data-ttu-id="03845-103">Usando a biblioteca COM</span><span class="sxs-lookup"><span data-stu-id="03845-103">Using the COM Library</span></span>

<span data-ttu-id="03845-104">A referência de biblioteca gerenciada do Tablet PC agora pode ser encontrada na seção referência da biblioteca de classes do SDK do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03845-104">The Tablet PC managed library reference can now be found in the regular Windows Vista SDK Class Library reference section.</span></span> <span data-ttu-id="03845-105">Ele fornece um modelo de objeto para Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="03845-105">It provides an object model for Microsoft Visual C++.</span></span> <span data-ttu-id="03845-106">A maioria dos objetos na biblioteca COM são idênticos aos encontrados na API gerenciada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="03845-106">The majority of the objects in the COM Library are identical to those found in the Tablet PC Managed API.</span></span>

<span data-ttu-id="03845-107">No entanto, a API COM contém alguns membros além daqueles encontrados na API gerenciada devido às diferenças entre o ambiente padrão do Microsoft Win32 e o ambiente do SDK do Microsoft .NET (Kit de desenvolvimento do Frameworksoftware).</span><span class="sxs-lookup"><span data-stu-id="03845-107">However, the COM API contains some members in addition to those found in the Managed API because of differences between the standard Microsoft Win32 environment and the Microsoft .NET Frameworksoftware development kit (SDK) environment.</span></span> <span data-ttu-id="03845-108">Por exemplo, os objetos InkRectangle e InkTransform são usados em COM, mas o FrameworkSDK fornece implementação nativa para [**classe InkRectangle**](inkrectangle-class.md) e [**classe InkTransform**](inktransform-class.md) que elimina a necessidade desses objetos na API gerenciada da plataforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="03845-108">For example, the InkRectangle and InkTransform objects are used in COM, but the FrameworkSDK provides native implementation for [**InkRectangle Class**](inkrectangle-class.md) and [**InkTransform Class**](inktransform-class.md) that eliminates the need for these objects in the Tablet PC platform Managed API.</span></span>

> [!Note]  
> <span data-ttu-id="03845-109">Os objetos na API COM e os controles de tinta não são projetados para uso em páginas de Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="03845-109">The objects in the COM API and the ink controls are not designed for use in Active Server Pages (ASP).</span></span>

 

## <a name="working-with-collections"></a><span data-ttu-id="03845-110">Trabalhando com coleções</span><span class="sxs-lookup"><span data-stu-id="03845-110">Working with Collections</span></span>

<span data-ttu-id="03845-111">Se você passar um valor **nulo** como o índice para qualquer um dos objetos de coleção na biblioteca com, você receberá o primeiro item na coleção porque esses valores de argumento são forçados a 0 quando a chamada é feita.</span><span class="sxs-lookup"><span data-stu-id="03845-111">If you pass in a **NULL** value as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

<span data-ttu-id="03845-112">A propriedade **\_ NewEnum** está marcada como restrita na definição de IDL (linguagem de definição de interface) para as interfaces de coleção.</span><span class="sxs-lookup"><span data-stu-id="03845-112">The **\_NewEnum** property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.</span></span>

<span data-ttu-id="03845-113">Em C++, use um `For...` loop para iterar por meio de uma coleção, primeiro obtendo o comprimento da coleção.</span><span class="sxs-lookup"><span data-stu-id="03845-113">In C++, use a `For...` loop to iterate through a collection by first obtaining the collection's length.</span></span> <span data-ttu-id="03845-114">O exemplo a seguir mostra como iterar os traços de um objeto [**InkDisp**](inkdisp-class.md) , `pInk` .</span><span class="sxs-lookup"><span data-stu-id="03845-114">The example below shows how to iterate through the strokes of an [**InkDisp**](inkdisp-class.md) object, `pInk`.</span></span>


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



## <a name="parameters"></a><span data-ttu-id="03845-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03845-115">Parameters</span></span>

<span data-ttu-id="03845-116">Se você passar o VT \_ vazio ou \_ o VT nulo como o índice para qualquer um dos objetos de coleção na biblioteca com, você receberá o primeiro item na coleção porque esses valores de argumento são forçados a 0 quando a chamada é feita.</span><span class="sxs-lookup"><span data-stu-id="03845-116">If you pass in VT\_EMPTY or VT\_NULL as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

## <a name="using-idispatch"></a><span data-ttu-id="03845-117">Usando IDispatch</span><span class="sxs-lookup"><span data-stu-id="03845-117">Using IDispatch</span></span>

<span data-ttu-id="03845-118">Para aumentar o desempenho, a API (interface de programação de aplicativo) COM do Tablet PC Platform não oferece suporte à chamada `IDispatchImpl::Invoke` com uma estrutura DISPPARAMS com argumentos nomeados.</span><span class="sxs-lookup"><span data-stu-id="03845-118">To increase performance, the Tablet PC Platform COM application programming interface (API) does not support calling `IDispatchImpl::Invoke` with a DISPPARAMS structure with named arguments.</span></span> <span data-ttu-id="03845-119">O `IDispatchImpl::GetIDsOfNames` também não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="03845-119">The `IDispatchImpl::GetIDsOfNames` is also not supported.</span></span> <span data-ttu-id="03845-120">Em vez disso, chame `Invoke` com os DISPIDs fornecidos nos cabeçalhos do SDK.</span><span class="sxs-lookup"><span data-stu-id="03845-120">Instead, call `Invoke` with the DISPIDs supplied in the SDK headers.</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="03845-121">Aguardando eventos</span><span class="sxs-lookup"><span data-stu-id="03845-121">Waiting for Events</span></span>

<span data-ttu-id="03845-122">O ambiente do Tablet PC é multithread.</span><span class="sxs-lookup"><span data-stu-id="03845-122">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="03845-123">Consulte a documentação COM para vários threads.</span><span class="sxs-lookup"><span data-stu-id="03845-123">Refer to COM documentation for multi-threading.</span></span>

## <a name="support-for-aggregation"></a><span data-ttu-id="03845-124">Suporte para agregação</span><span class="sxs-lookup"><span data-stu-id="03845-124">Support for Aggregation</span></span>

<span data-ttu-id="03845-125">A agregação foi testada apenas para o controle [InkEdit](inkedit-control-reference.md) , o controle [InkPicture](inkpicture-control-reference.md) , o objeto [**InkDisp**](inkdisp-class.md) e o objeto [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="03845-125">Aggregation has been tested for only the [InkEdit](inkedit-control-reference.md) control, the [InkPicture](inkpicture-control-reference.md) control, the [**InkDisp**](inkdisp-class.md) object, and the [**InkOverlay**](inkoverlay-class.md) object.</span></span> <span data-ttu-id="03845-126">A agregação não foi testada para outros controles e objetos na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="03845-126">Aggregation has not been tested for other controls and objects in the library.</span></span>

## <a name="c"></a><span data-ttu-id="03845-127">C++</span><span class="sxs-lookup"><span data-stu-id="03845-127">C++</span></span>

<span data-ttu-id="03845-128">Usar o SDK do Tablet PC em C++ requer o uso de alguns conceitos COM, como VARIANT, SAFEARRAY e BSTR.</span><span class="sxs-lookup"><span data-stu-id="03845-128">Using the Tablet PC SDK in C++ requires the use of some COM concepts, such as VARIANT, SAFEARRAY, and BSTR.</span></span> <span data-ttu-id="03845-129">Esta seção descreve como usá-los.</span><span class="sxs-lookup"><span data-stu-id="03845-129">This section describes how to use them.</span></span>

### <a name="variant-and-safearray"></a><span data-ttu-id="03845-130">VARIANTE e SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="03845-130">VARIANT and SAFEARRAY</span></span>

<span data-ttu-id="03845-131">A estrutura variante é usada para comunicação entre objetos COM.</span><span class="sxs-lookup"><span data-stu-id="03845-131">The VARIANT structure is used for communication between COM objects.</span></span> <span data-ttu-id="03845-132">Essencialmente, a estrutura variante é um contêiner para uma União grande que transporta muitos tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="03845-132">Essentially, the VARIANT structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="03845-133">O valor no primeiro membro da estrutura, VT, descreve qual dos membros da União é válido.</span><span class="sxs-lookup"><span data-stu-id="03845-133">The value in the first member of the structure, vt, describes which of the union members is valid.</span></span> <span data-ttu-id="03845-134">Ao receber informações em uma estrutura de variante, verifique o membro VT para descobrir qual membro contém dados válidos.</span><span class="sxs-lookup"><span data-stu-id="03845-134">When you receive information in a VARIANT structure, check the vt member to find out which member contains valid data.</span></span> <span data-ttu-id="03845-135">Da mesma forma, quando você envia informações usando uma estrutura VARIANT, sempre defina VT para refletir o membro Union que contém as informações.</span><span class="sxs-lookup"><span data-stu-id="03845-135">Similarly, when you send information using a VARIANT structure, always set vt to reflect the union member that contains the information.</span></span>

<span data-ttu-id="03845-136">Antes de usar a estrutura, inicialize-a chamando a função COM VariantInit.</span><span class="sxs-lookup"><span data-stu-id="03845-136">Before using the structure, initialize it by calling the VariantInit COM function.</span></span> <span data-ttu-id="03845-137">Quando terminar com a estrutura, limpe-a antes que a memória que contém a variante seja liberada chamando VariantClear.</span><span class="sxs-lookup"><span data-stu-id="03845-137">When finished with the structure, clear it before the memory that contains the VARIANT is freed by calling VariantClear.</span></span>

<span data-ttu-id="03845-138">Para obter mais informações sobre a estrutura de variante, consulte [tipos de dados Variant e VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="03845-138">For more information on the VARIANT structure, see [VARIANT and VARIANTARG Data Types](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="03845-139">A estrutura SAFEARRAY é fornecida como uma maneira de trabalhar com segurança com matrizes no COM.</span><span class="sxs-lookup"><span data-stu-id="03845-139">The SAFEARRAY structure is provided as a way to safely work with arrays in COM.</span></span> <span data-ttu-id="03845-140">O campo pArray da variante é um ponteiro para um SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="03845-140">The VARIANT's parray field is a pointer to a SAFEARRAY.</span></span> <span data-ttu-id="03845-141">Use funções como SafeArrayCreateVector, SafeArrayAccessData e SafeArrayUnaccessData para criar e preencher um SAFEARRAY em uma variante.</span><span class="sxs-lookup"><span data-stu-id="03845-141">Use functions such as SafeArrayCreateVector, SafeArrayAccessData, and SafeArrayUnaccessData to create and fill a SAFEARRAY in a VARIANT.</span></span>

<span data-ttu-id="03845-142">Para obter mais informações sobre o tipo de dados SAFEARRAY, consulte [tipo de dados SafeArray](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="03845-142">For more information on the SAFEARRAY data type, see [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

<span data-ttu-id="03845-143">Este exemplo de C++ cria um [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` , em um objeto [**InkDisp**](inkdisp-class.md) , `pInk` , de uma matriz de dados Point.</span><span class="sxs-lookup"><span data-stu-id="03845-143">This C++ example creates an [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp`, in an [**InkDisp**](inkdisp-class.md) object, `pInk`, from an array of point data.</span></span>


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



### <a name="bstr"></a><span data-ttu-id="03845-144">BSTR</span><span class="sxs-lookup"><span data-stu-id="03845-144">BSTR</span></span>

<span data-ttu-id="03845-145">O formato de cadeia de caracteres com suporte para COM é BSTR.</span><span class="sxs-lookup"><span data-stu-id="03845-145">The supported string format for COM is BSTR.</span></span> <span data-ttu-id="03845-146">Um BSTR tem um ponteiro para uma cadeia de caracteres terminada em zero, mas também contém o comprimento da cadeia de caracteres (em bytes, não contando o terminador), que é armazenado nos 4 bytes imediatamente antes do primeiro caractere da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="03845-146">A BSTR has a pointer to a zero-terminated string, but it also contains the length of the string (in bytes, not counting the terminator), which is stored in the 4 bytes immediately preceding the first character of the string.</span></span>

<span data-ttu-id="03845-147">Para obter mais informações sobre BSTR, consulte [tipo de dados BSTR](/previous-versions/windows/desktop/automat/bstr).</span><span class="sxs-lookup"><span data-stu-id="03845-147">For more information on BSTR, see [BSTR Data Type](/previous-versions/windows/desktop/automat/bstr).</span></span>

<span data-ttu-id="03845-148">Este exemplo de C++ mostra como definir o factor em um [**InkRecognizerContext**](inkrecognizercontext-class.md) usando um BSTR.</span><span class="sxs-lookup"><span data-stu-id="03845-148">This C++ sample shows how to set the factoid on an [**InkRecognizerContext**](inkrecognizercontext-class.md) using a BSTR.</span></span>


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



 

 
