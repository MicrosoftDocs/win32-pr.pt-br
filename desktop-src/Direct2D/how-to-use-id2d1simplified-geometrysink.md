---
title: Como recuperar dados de geometria estendendo ID2D1SimplifiedGeometrySink
description: Mostra como recuperar dados de geometria estendendo a interface ID2D1SimplifiedGeometrySink.
ms.assetid: c6777b11-6d4e-409e-9c30-da1e060c9aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba3670eb8d0152cc1dae8fbcc164bd8a6167630
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007969"
---
# <a name="how-to-retrieve-geometry-data-by-extending-id2d1simplifiedgeometrysink"></a><span data-ttu-id="abebc-103">Como recuperar dados de geometria estendendo ID2D1SimplifiedGeometrySink</span><span class="sxs-lookup"><span data-stu-id="abebc-103">How to Retrieve Geometry Data by Extending ID2D1SimplifiedGeometrySink</span></span>

<span data-ttu-id="abebc-104">Embora um objeto [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) seja imutável, há casos em que você precisa manipular os dados de geometria em um objeto de geometria de caminho.</span><span class="sxs-lookup"><span data-stu-id="abebc-104">While an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object is immutable, there are cases where you need to manipulate the geometry data in a path geometry object.</span></span> <span data-ttu-id="abebc-105">O Direct2D permite que você faça isso fornecendo uma interface extensível chamada [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span><span class="sxs-lookup"><span data-stu-id="abebc-105">Direct2D enables you to do so by providing an extendable interface named [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span> <span data-ttu-id="abebc-106">Para a ilustração de conceito, este tópico descreve como estender essa interface para recuperar os dados de geometria de um objeto de geometria de caminho.</span><span class="sxs-lookup"><span data-stu-id="abebc-106">For concept illustration, this topic describes how to extend this interface to retrieve the geometry data from a path geometry object.</span></span>

<span data-ttu-id="abebc-107">**Para estender a interface ID2D1SimplifiedGeometrySink**</span><span class="sxs-lookup"><span data-stu-id="abebc-107">**To Extend the ID2D1SimplifiedGeometrySink interface**</span></span>

1.  <span data-ttu-id="abebc-108">Implemente uma classe que herde de [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span><span class="sxs-lookup"><span data-stu-id="abebc-108">Implement a class that inherits from [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).</span></span>
2.  <span data-ttu-id="abebc-109">Crie uma instância dessa classe e passe-a para [**ID2D1Geometry:: simplificar**](id2d1geometry-simplify.md).</span><span class="sxs-lookup"><span data-stu-id="abebc-109">Create an instance of that class and pass it to [**ID2D1Geometry::Simplify**](id2d1geometry-simplify.md).</span></span>

<span data-ttu-id="abebc-110">O exemplo de código a seguir mostra como implementar uma classe chamada SpecializedSink que herda da interface [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) .</span><span class="sxs-lookup"><span data-stu-id="abebc-110">The following code example shows how to implement a class named SpecializedSink that inherits from the [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) interface.</span></span> <span data-ttu-id="abebc-111">Para a simplicidade da ilustração de conceito, o método **AddLines** estendido recupera os dados de geometria e, em seguida, exibe-os na janela do console; Você pode personalizar esse método para atender às suas necessidades de dados específicas.</span><span class="sxs-lookup"><span data-stu-id="abebc-111">For the simplicity of concept illustration, the extended **AddLines** method retrieves the geometry data and then displays it on the console window; you can customize this method to meet your specific data needs.</span></span>


```C++
class SpecializedSink : public ID2D1SimplifiedGeometrySink
{
    public:
        SpecializedSink()
            : m_cRef(1)
        {
        }

        STDMETHOD_(ULONG, AddRef)(THIS)
        {
            return InterlockedIncrement(reinterpret_cast<LONG volatile *>(&m_cRef));
        }

        STDMETHOD_(ULONG, Release)(THIS)
        {
            ULONG cRef = static_cast<ULONG>(
            InterlockedDecrement(reinterpret_cast<LONG volatile *>(&m_cRef)));

            if(0 == cRef)
            {
                delete this;
            }

            return cRef;
        }

        STDMETHOD(QueryInterface)(THIS_ REFIID iid, void** ppvObject)
        {
            HRESULT hr = S_OK;

            if (__uuidof(IUnknown) == iid)
            {
                *ppvObject = static_cast<IUnknown*>(this);
                AddRef();
            }
            else if (__uuidof(ID2D1SimplifiedGeometrySink) == iid)
            {
                *ppvObject = static_cast<ID2D1SimplifiedGeometrySink*>(this);
                AddRef();
            }
            else
            {
                *ppvObject = NULL;
                hr = E_NOINTERFACE;
            }

            return hr;
        }

        STDMETHOD_(void, AddBeziers)(const D2D1_BEZIER_SEGMENT * /*beziers*/,
                                     UINT /*beziersCount*/)
        {
            // Customize this method to meet your specific data needs.
        }

        STDMETHOD_(void, AddLines)(const D2D1_POINT_2F *points, UINT pointsCount)
        {
            // Customize this method to meet your specific data needs.
            printf("\n\nRetrieving geometry data from a derived ID2D1SimplifiedGeometrySink object:\n");
            for (UINT i = 0; i < pointsCount; ++i)
            {
                printf("%.0f, %.0f\n", points[i].x, points[i].y);
            }
        }

        STDMETHOD_(void, BeginFigure)(D2D1_POINT_2F startPoint,
                                      D2D1_FIGURE_BEGIN figureBegin)
        {
        }

        STDMETHOD_(void, EndFigure)(D2D1_FIGURE_END figureEnd)
        {
        }

        STDMETHOD_(void, SetFillMode)(D2D1_FILL_MODE fillMode)
        {
        }

        STDMETHOD_(void, SetSegmentFlags)(D2D1_PATH_SEGMENT vertexFlags)
        {
        }

        STDMETHOD(Close)()
        {
            return S_OK;
        }

    private:
        UINT m_cRef;
};
```



<span data-ttu-id="abebc-112">Em seguida, o exemplo usa um conjunto de dados (182, 209), (211, 251), (251, 226), (392, 360) e (101, 360) para criar uma geometria de caminho populada (**m \_ pGeometry**) onde os dados podem ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="abebc-112">The example then uses a set of data (182, 209), (211, 251), (251, 226), (392, 360), and (101, 360) to create a populated path geometry (**m\_pGeometry**) where data can be retrieved.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pGeometry);
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;

    hr = m_pGeometry->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

        pSink->BeginFigure(
            D2D1::Point2F(101,360),
            D2D1_FIGURE_BEGIN_FILLED
            );
        D2D1_POINT_2F points[5] = {
           D2D1::Point2F(182,209),
           D2D1::Point2F(211,251),
           D2D1::Point2F(251,226),
           D2D1::Point2F(392,360),
           D2D1::Point2F(101,360),
           };

        printf("Adding the following geometry data to an ID2D1GeometrySink object:\n");
        printf("182, 209\n");
        printf("211, 251\n");
        printf("251, 226\n");
        printf("392, 360\n");
        printf("101, 360\n");

        pSink->AddLines(points, ARRAYSIZE(points));
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
        pSink->Release();
```



<span data-ttu-id="abebc-113">Por fim, o exemplo cria um objeto SpecializedSink e, em seguida, chama o método [**ID2D1Geometry:: simplificar**](id2d1geometry-simplify.md) , passando o objeto SpecializedSink e o parâmetro de [**\_ linhas da \_ \_ opção \_ de simplificação de geometria d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option) , que faz com que as curvas sejam achatadas em segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="abebc-113">Finally, the example creates a SpecializedSink object, and then calls the [**ID2D1Geometry::Simplify**](id2d1geometry-simplify.md) method, passing in the SpecializedSink object and the [**D2D1\_GEOMETRY\_SIMPLIFICATION\_OPTION\_LINES**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_simplification_option) parameter, which causes any curves to be flattened into line segments.</span></span>


```C++
        SpecializedSink *pSpecializedSink = NULL;

        if (SUCCEEDED(hr))
        {
            pSpecializedSink = new SpecializedSink();
            if (!pSpecializedSink)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        if (SUCCEEDED(hr))
        {
            hr = m_pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES, // This causes any curves to be flattened into line segments.
                    NULL, // world transform
                    pSpecializedSink
                    );


            if (SUCCEEDED(hr))
            {
                hr = pSpecializedSink->Close();
            }

            pSpecializedSink->Release();
        }
```



<span data-ttu-id="abebc-114">O programa cria saídas conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="abebc-114">The program creates outputs as shown in the following screen shot.</span></span>

![captura de tela de uma janela de console com saída sobre como adicionar e recuperar dados de geometria](images/specializedgeometrysink.png)

## <a name="related-topics"></a><span data-ttu-id="abebc-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abebc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abebc-117">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="abebc-117">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 