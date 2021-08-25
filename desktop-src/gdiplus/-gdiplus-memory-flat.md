---
description: Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções de API simples são empacotadas pela classe GdiplusBase C++.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funções de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce4e75de3cf5c7ff96a794416b75a9bacadda5a0aade2f5a61e2607e620e3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943806"
---
# <a name="memory-functions"></a>Funções de memória

Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat.h. As funções no GDI+ API simples são envolvidas por uma coleção de cerca de 40 classes C++. É recomendável que você não chame diretamente as funções na API simples. Sempre que fizer chamadas para GDI+, você deverá fazer isso chamando os métodos e funções fornecidos pelos wrappers do C++. Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente. Para obter mais informações sobre como usar esses métodos wrapper, [consulte GDI+ API Simples.](-gdiplus-flatapi-flat.md)

As funções de API simples a seguir são empacotadas pela [**classe C++ GdiplusBase.**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase)

## <a name="memory-functions-and-corresponding-wrapper-methods"></a>Funções de memória e métodos de wrapper correspondentes



| Função simples                                          | Método Wrapper                                                                                                                                      | Comentários                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipAlloc (tamanho \_ t size)<br/> | [**GpStatus WINGDIPAPI GdiplusBase void \* (operador new)(size \_ t in \_ size)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | Aloca memória para um Windows GDI+ objeto . <br/> GdipAlloc é declarado em GdiplusMem.h.<br/>  |
| GpStatus WINGDIPAPI GdipFree(void \* ptr);<br/>   | [**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void \* em \_ pVoid)**](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | Desaloca a memória para um Windows GDI+ objeto . <br/> GdipFree é declarado em GdiplusMem.h.<br/> |



 

 

 
