---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções simples de API são encapsuladas pela classe GdiplusBase C++.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funções de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395821"
---
# <a name="memory-functions"></a>Funções de memória

O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h. As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++. O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).

As funções de API simples a seguir são encapsuladas pela classe [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++.

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Funções de memória e métodos de wrapper correspondentes



| Função Flat                                          | Método de wrapper                                                                                                                                      | Comentários                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc (tamanho \_ t tamanho)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (novo operador) (tamanho \_ em \_ tamanho)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Aloca memória para um objeto Windows GDI+. <br/> GdipAlloc é declarado em GdiplusMem. h.<br/>  |
| GpStatus WINGDIPAPI GdipFree (void \* PTR);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (operador Delete) (void \* em \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Desaloca memória para um objeto Windows GDI+. <br/> GdipFree é declarado em GdiplusMem. h.<br/> |



 

 

 
