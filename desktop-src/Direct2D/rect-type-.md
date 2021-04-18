---
title: Função Rect Type (D2d1helper. h)
description: Cria uma estrutura de retângulo que armazena suas coordenadas usando o tipo de dados especificado.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Função de tipo Rect Direct2D
topic_type:
- apiref
api_name:
- Rect Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ed16ecd5a79c73ecb7341b9aa7f3378854dd4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749863"
---
# <a name="recttype-function"></a><Type>Função Rect

Cria uma estrutura de retângulo que armazena suas coordenadas usando o tipo de dados especificado.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Rect Rect(
  Type left,
  Type top,
  Type right,
  Type bottom
);
```

## <a name="template-parameters"></a>Parâmetros de modelo



| Parâmetro | Descrição                                                                                                |
|-----------|------------------------------------------------------------------------------------------------------------|
| Type      | O tipo de dados usado para armazenar as dimensões do retângulo. Os valores possíveis são **float** e **UINT32**. |



 

## <a name="parameters"></a>Parâmetros



| Parâmetro | Descrição                                             |
|-----------|---------------------------------------------------------|
| esquerda      | A coordenada x do canto superior esquerdo do retângulo.  |
| top       | A coordenada y do canto superior esquerdo do retângulo.  |
| direita     | A coordenada x do canto inferior direito do retângulo. |
| parte inferior    | A coordenada y do canto inferior direito do retângulo. |



 

## <a name="return-value"></a>Valor Retornado

Uma estrutura de retângulo que contém as coordenadas especificadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





