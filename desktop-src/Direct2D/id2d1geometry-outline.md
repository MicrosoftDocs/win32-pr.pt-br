---
title: Métodos de estrutura de tópicos ID2D1Geometry
description: Computa o contorno da geometria e grava o resultado em um ID2D1SimplifiedGeometrySink.
ms.assetid: ec92db79-a1aa-4661-9e75-45a1763af370
keywords:
- Métodos de estrutura de tópicos Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 40d4ff1122d4a00e11ea35914f001b6dc9e06e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755804"
---
# <a name="id2d1geometryoutline-methods"></a>Métodos ID2D1Geometry:: outline

Computa o contorno da geometria e grava o resultado em um [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                          | Descrição                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Estrutura de tópicos (D2D1 \_ Matrix \_ 3X2 \_ F&, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Computa o contorno da geometria e grava o resultado em um [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). <br/> |
| [**Estrutura de tópicos ( \_ matriz d2d1 \_ 3x2 \_ F \* , ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Computa o contorno da geometria e grava o resultado em um [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Contorno ( \_ matriz d2d1 \_ 3X2 \_ F&, float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Computa o contorno da geometria e grava o resultado em um [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Outline ( \_ matriz d2d1 \_ 3x2 \_ F \* , float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Computa o contorno da geometria e grava o resultado em um [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |



## <a name="remarks"></a>Comentários

O método [**outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) permite que o chamador produza uma geometria com um preenchimento equivalente para a geometria de entrada, com as seguintes propriedades adicionais:

-   A geometria de saída não contém interseções de transversal; ou seja, os segmentos podem tocar, mas nunca cruzam.
-   Os números mais externos na geometria de saída são todos orientados no sentido anti-horário.
-   A geometria de saída é invariável de modo de preenchimento; ou seja, o preenchimento da geometria não depende da escolha do modo de preenchimento. Para obter mais informações sobre o modo de preenchimento, consulte [**\_ \_ modo de preenchimento d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode).

Além disso, o método de [**estrutura de tópicos**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) pode ser útil para remover partes redundantes de geometrias para simplificar geometrias complexas. Ele também pode ser útil em combinação com [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) para criar uniões entre várias geometrias simultaneamente.

## <a name="examples"></a>Exemplos

O código a seguir mostra como usar a **estrutura de tópicos** para construir uma geometria equivalente sem interseções automáticas. Ele usa a tolerância de nivelamento padrão e, portanto, não deve ser usado com geometrias muito pequenas.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

