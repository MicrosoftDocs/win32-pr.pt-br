---
title: Método IDWriteFontFallback MapCharacters
description: Determina uma fonte apropriada a ser usada para renderizar o intervalo inicial de texto.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Gravação direta do método MapCharacters
- Método MapCharacters Direct Write, interface IDWriteFontFallback
- IDWriteFontFallback interface de gravação direta, método MapCharacters
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99f18932121d44f61d67c8124faa2d26638035bdcff473ad26c4222ceea9a85b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048786"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>Método IDWriteFontFallback:: MapCharacters

Determina uma fonte apropriada a ser usada para renderizar o intervalo inicial de texto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*source* 
</dt> <dd>

Tipo: **[ **IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\***

A implementação da fonte de texto contém o texto e a localidade.

</dd> <dt>

*textPosition* 
</dt> <dd>

Tipo: **UINT32**

Posição inicial para analisar.

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UINT32**

Comprimento do texto a ser analisado.

</dd> <dt>

*baseFontCollection* \[ em, opcional\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\***

Coleção de fontes padrão a ser usada.

</dd> <dt>

*baseFamilyName* \[ em, opcional\]
</dt> <dd>

Tipo: **const WCHAR \_ t \***

Nome da família da fonte base. Se você passar NULL, nenhuma correspondência será feita em relação à família.

</dd> <dt>

*baseWeight* 
</dt> <dd>

Tipo: **[ **\_ \_ espessura da fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

O peso desejado.

</dd> <dt>

*basestyle* 
</dt> <dd>

Tipo: **[ **\_ \_ estilo de fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

O estilo desejado.

</dd> <dt>

*baseStretch* 
</dt> <dd>

Tipo: **[ **DWRITE \_ fonte \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

A ampliação desejada.

</dd> <dt>

*mappedLength* \[ fora\]
</dt> <dd>

Tipo: **UINT32 \***

Comprimento do texto mapeado para a fonte mapeada. Isso sempre será menor ou igual ao tamanho do texto e maior que zero (se o comprimento do texto for diferente de zero), o chamador avançará pelo menos um caractere.

</dd> <dt>

*mappedFont* \[ fora\]
</dt> <dd>

Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

A fonte que deve ser usada para renderizar os primeiros caracteres *mappedLength* do texto. Se ele retornar NULL, isso significa que nenhuma fonte pode renderizar o texto e *mappedLength* é o número de caracteres a serem ignorados (renderizado com um glifo ausente).

</dd> <dt>

*escala* \[ fora\]
</dt> <dd>

Tipo: **float \***

Fator de escala para multiplicar o tamanho em em da fonte retornada por.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                 |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

