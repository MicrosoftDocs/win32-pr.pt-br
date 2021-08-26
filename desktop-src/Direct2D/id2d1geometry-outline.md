---
title: Métodos de Contorno de ID2D1Geometry
description: Calcula o contorno da geometria e grava o resultado em um ID2D1SimplifiedGeometrySink.
ms.assetid: ec92db79-a1aa-4661-9e75-45a1763af370
keywords:
- Métodos de contorno Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 3c10a777d33e0a8c9a9fa033ca2615ce2d45b2badd292757e90f88074e131549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917906"
---
# <a name="id2d1geometryoutline-methods"></a>Métodos ID2D1Geometry::Outline

Calcula o contorno da geometria e grava o resultado em [**um ID2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                                                          | Descrição                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ F&,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Calcula o contorno da geometria e grava o resultado em [**um ID2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) <br/> |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ \* F, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Calcula o contorno da geometria e grava o resultado em [**um ID2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ F&,FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Calcula o contorno da geometria e grava o resultado em [**um ID2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |
| [**Outline(D2D1 \_ MATRIX \_ 3X2 \_ \* F, FLOAT,ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Calcula o contorno da geometria e grava o resultado em [**um ID2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)<br/>  |



## <a name="remarks"></a>Comentários

O [**método Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) permite que o chamador produza uma geometria com um preenchimento equivalente à geometria de entrada, com as seguintes propriedades adicionais:

-   A geometria de saída não contém interseções de transverso; ou seja, os segmentos podem tocar, mas nunca se cruzam.
-   As figuras mais externas na geometria de saída são todas orientadas no sentido anti-horário.
-   A geometria de saída é invariável no modo de preenchimento; ou seja, o preenchimento da geometria não depende da escolha do modo de preenchimento. Para obter mais informações sobre o modo de preenchimento, consulte [**MODO DE PREENCHIMENTO D2D1 \_ \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode).

Além disso, o [**método Outline**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) pode ser útil na remoção de partes redundantes de geometrias comentadas para simplificar geometrias complexas. Também pode ser útil em combinação com [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) para criar uniões entre várias geometrias simultaneamente.

## <a name="examples"></a>Exemplos

O código a seguir mostra como usar **Outline** para construir uma geometria equivalente sem autoseções. Ele usa a tolerância de nivelamento padrão e, portanto, não deve ser usado com geometrias muito pequenas.


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
| Biblioteca<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

