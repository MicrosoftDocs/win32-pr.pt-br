---
title: Métodos ID2D1Geometry ComputeLength
description: Calcula o comprimento da geometria como se cada segmento fosse revertido em uma linha.
ms.assetid: 4659d880-0aa3-485d-ac71-044d9ace6759
keywords:
- Métodos ComputeLength Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: b49b1beb0525d95967ad903b0f0fb3c464edf4d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747624"
---
# <a name="id2d1geometrycomputelength-methods"></a>Métodos ID2D1Geometry:: ComputeLength

Calcula o comprimento da geometria como se cada segmento fosse revertido em uma linha.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                                          | Descrição                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**ComputeLength ( \_ matriz d2d1 \_ 3X2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))              | Calcula o comprimento da geometria como se cada segmento fosse revertido em uma linha.<br/>  |
| [**ComputeLength ( \_ matriz d2d1 \_ 3x2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float))             | Calcula o comprimento da geometria como se cada segmento fosse revertido em uma linha.<br/>  |
| [**ComputeLength ( \_ matriz d2d1 \_ 3X2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f__float_float))  | Calcula o comprimento da geometria como se cada segmento fosse revertido em uma linha.<br/>  |
| [**ComputeLength ( \_ matriz d2d1 \_ 3x2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computelength(constd2d1_matrix_3x2_f_float)) | Calcula o comprimento da geometria como se cada segmento fosse revertido em uma linha. <br/> |



## <a name="examples"></a>Exemplos

O código a seguir mostra como usar **ComputeLength** para calcular o comprimento de uma geometria de caminho especificada.


```C++
float length = 0;
hr = m_pPathGeometry->ComputeLength(
    NULL, //no transform
    &length
    );

if (SUCCEEDED(hr))
{
    m_Animation.SetStart(0);        //start at beginning of path
    m_Animation.SetEnd(length);     //length at end of path
    m_Animation.SetDuration(5.0f);  //seconds

    ZeroMemory(&m_DwmTimingInfo, sizeof(m_DwmTimingInfo));
    m_DwmTimingInfo.cbSize = sizeof(m_DwmTimingInfo);

    // Get the composition refresh rate. If the DWM isn't running,
    // get the refresh rate from GDI -- probably going to be 60Hz
    if (FAILED(DwmGetCompositionTimingInfo(NULL, &m_DwmTimingInfo)))
    {
        HDC hdc = GetDC(m_hwnd);
        m_DwmTimingInfo.rateCompose.uiDenominator = 1;
        m_DwmTimingInfo.rateCompose.uiNumerator = GetDeviceCaps(hdc, VREFRESH);
        ReleaseDC(m_hwnd, hdc);
    }

    ShowWindow(m_hwnd, SW_SHOWNORMAL);

    UpdateWindow(m_hwnd);
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

 

