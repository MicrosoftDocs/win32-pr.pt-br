---
title: Direct2D constantes
description: Direct2D define a lista de constantes a seguir.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: cd8adfa3d6fa3c59a05331c82ea12100918a4697d9478097a890eedff039d5e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768726"
---
# <a name="direct2d-constants"></a>Direct2D constantes

As constantes a seguir são declaradas nos `d2d1effectauthor.h` arquivos de cabeçalho,, `d2d1.h` `d2d1_1.h` e `d2d1effects_2.h` .

## <a name="d2d1_append_aligned_element--1"></a>D2D1_APPEND_ALIGNED_ELEMENT (-1)
Usado ao empacotar elementos de layout de entrada. Ele indica que os elementos devem ser empacotados de forma contígua.

## <a name="d2d1_default_flattening_tolerance-025f"></a>D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)
A tolerância padrão para operações de mesclagem geométricas.

## <a name="d2d1_invalid_property_index-uint_max"></a>D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)
Define um índice de propriedade inválido.

Essa constante é retornada de [**ID2D1Properties:: GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) para indicar que a propriedade nomeada que você forneceu não tem um índice na interface de propriedade.

Se você passar essa constante para [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) ou [**ID2D1Properties:: GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), a chamada falhará e o buffer de saída será preenchido com zero.

## <a name="d2d1_invalid_tag-ulonglong_max"></a>D2D1_INVALID_TAG (ULONGLONG_MAX)
Reservado Não use.

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a>D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0 f)
O número de nits que o espaço de cores sRGB ou scRGB usa para o SDR branco ou valores de ponto flutuante de 1,0 f. Esse valor é constante somente quando o espaço de cores usa a luminância referida pela cena, que é verdadeira para conteúdo de intervalo dinâmico alto (HDR). Se o espaço de cores usar a luminância de exibição referenciada, o nível de branco do SDR deverá ser consultado a partir da exibição.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| Cliente mínimo com suporte | Windows 7, Windows vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ desktop apps \|\] |
| Servidor mínimo com suporte | Windows server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos do Windows Server 2008 \[ desktop aplicativos \| UWP\] |
| Número mínimo de telefone com suporte | Windows Phone 8,1 \[ Windows Phone silverlight 8,1 e aplicativos \] de Windows Runtime, Windows Phone 8,1 \[ Windows Phone silverlight 8,1 e aplicativos de Windows Runtime\] |
| Cabeçalho | d2d1effectauthor. h, d2d1. h, d2d1_1. h, d2d1effects_2. h |
