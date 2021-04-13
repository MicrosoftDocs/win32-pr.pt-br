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
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295815"
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

Tipo: **[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _

A implementação da fonte de texto contém o texto e a localidade.

</dd> <dt>

_textPosition * 
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

Tipo: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _

Coleção de fontes padrão a ser usada.

</dd> <dt>

_baseFamilyName * \[ in, opcional\]
</dt> <dd>

Tipo: **const WCHAR \_ t \** _

Nome da família da fonte base. Se você passar NULL, nenhuma correspondência será feita em relação à família.

</dd> <dt>

_baseWeight * 
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

Tipo: **UINT32 \** _

Comprimento do texto mapeado para a fonte mapeada. Isso sempre será menor ou igual ao tamanho do texto e maior que zero (se o comprimento do texto for diferente de zero), o chamador avançará pelo menos um caractere.

</dd> <dt>

_mappedFont * \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

A fonte que deve ser usada para renderizar os primeiros caracteres *mappedLength* do texto. Se ele retornar NULL, isso significa que nenhuma fonte pode renderizar o texto e *mappedLength* é o número de caracteres a serem ignorados (renderizado com um glifo ausente).

</dd> <dt>

*escala* \[ fora\]
</dt> <dd>

Tipo: **float \** _

Fator de escala para multiplicar o tamanho em em da fonte retornada por.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                 |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

