---
title: Direct2D funções
description: Direct2D fornece as funções a seguir.
ms.assetid: 1a7ae962-9b70-442c-a676-f172a2d9bfd3
keywords:
- Direct2D, funções
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 7df417bbaba8c442f61005b35900641c379da9d7b61fa91e898d41e0d73821d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874476"
---
# <a name="direct2d-functions"></a>Direct2D funções

Direct2D fornece as funções a seguir. Funções adicionais são definidas no [Namespace D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**D2D1ComputeMaximumScaleFactor**](/windows/desktop/api/d2d1_2/nf-d2d1_2-d2d1computemaximumscalefactor) | Calcula o fator máximo pelo qual uma determinada transformação pode alongar qualquer vetor. |
| [**D2D1CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) | Cria um novo Direct2D dispositivo associado ao dispositivo DXGI fornecido.  |
| [**D2D1CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext) | Cria um novo Direct2D de dispositivo associado a uma superfície DXGI.  |
| [**D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,void \* \* )**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory-r1) | Cria um objeto de fábrica que pode ser usado para criar Direct2D recursos. |
| [**D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,D2D1_FACTORY_OPTIONS \* ,void \* \* )**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) | Cria um objeto de fábrica que pode ser usado para criar Direct2D recursos. |
| [**D2D1GetGradientMeshInteriorPointsFromCoonsPatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-d2d1getgradientmeshinteriorpointsfromcoonspatch) | Retorna os pontos interiores de um patch de malha de gradiente com base nos pontos que definem um patch de Coons. |
| [**D2D1InvertMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1invertmatrix) | Tenta inverter a matriz especificada. |
| [**D2D1IsMatrixInvertible**](/windows/desktop/api/d2d1/nf-d2d1-d2d1ismatrixinvertible) | Indica se a matriz especificada é invertível. |
| [**D2D1MakeRotateMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makerotatematrix) | Cria uma transformação de rotação que gira pelo ângulo especificado sobre o ponto especificado. |
| [**D2D1MakeSkewMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makeskewmatrix) | Cria uma transformação de distorção que tem o ângulo do eixo x, o ângulo do eixo y e o ponto central especificados.  |
| [**operator \* (const D2D1\MATRIX\3X2\F&,const D2D1\MATRIX\3X2\F&)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-setproduct) | Multiplica duas matrizes e retorna o resultado. |
| [**BlobGetter**](blobgetter.md) | Chama um retorno de chamada getter de propriedade de função membro para uma propriedade de tipo blob. |
| [**BlobSetter**](blobsetter.md) | Chama um retorno de chamada de setter de propriedade de função membro para uma propriedade de tipo blob. |
| [**DeduçãoBlobGetter**](deducingblobgetter.md) | Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter da propriedade member-function para uma propriedade de tipo blob. |
| [**DeduçãoBlobSetter**](deducingblobsetter.md) | Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada de setter de propriedade de função membro para uma propriedade de tipo blob. |
| [**DeducingStringGetter**](deducingstringgetter.md) | Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter de propriedade de função de membro para uma propriedade de tipo de cadeia de caracteres. |
| [**DeducingStringSetter**](deducingstringsetter.md) | Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada de setter de propriedade de função de membro para uma propriedade de tipo de cadeia de caracteres. |
| [**DeducingValueGetter**](deducingvaluegetter.md) | Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada getter da propriedade member-function para uma propriedade de tipo de valor. |
| [**DeducingValueSetter**](deducingvaluesetter.md) | Deduz a classe e os argumentos e, em seguida, chama um retorno de chamada de setter de propriedade de função de membro para uma propriedade de tipo de valor. |
| [**Gettype**](/previous-versions/windows/desktop/legacy/hh847962(v=vs.85)) | Recupera o tipo da propriedade determinada. |
| [**StringGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringgetter) | Chama um retorno de chamada getter de propriedade de função membro para uma propriedade de tipo de cadeia de caracteres. |
| [**StringSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringsetter) | Chama um retorno de chamada de setter de propriedade de função membro para uma propriedade de tipo de cadeia de caracteres. |
| [**ValueGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuegetter) | Chama um retorno de chamada de setter de propriedade de função membro para uma propriedade de tipo de valor. |
| [**ValueSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuesetter) | Chama um retorno de chamada de setter de propriedade de função membro para uma propriedade de tipo de valor. |
| [**D2D1ConvertColorSpace**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1convertcolorspace) | Converte a cor determinada de um colorspace em outro. |
| [**D2D1SinCos**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1sincos) | Retorna o seno e o cosseno de um ângulo. |
| [**D2D1Tan**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1tan) | Retorna a tangente de um ângulo. |
| [**D2D1Vec3Length**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1vec3length) | Retorna o comprimento de um vetor tridimensional. |
| [**PD2D1\PROPERTY\GET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_get_function) | Obtém uma propriedade de um efeito. |
| [**PD2D1\PROPERTY\SET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_set_function) | Define uma propriedade em um efeito. |