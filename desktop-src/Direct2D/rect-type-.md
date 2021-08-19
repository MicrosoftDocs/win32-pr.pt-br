---
title: Função rect Type (D2d1helper.h)
description: Cria uma estrutura de retângulo que armazena suas coordenadas usando o tipo de dados especificado.
ms.assetid: b152efaf-0779-4024-b998-82a347abba71
keywords:
- Função rect Type Direct2D
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
ms.openlocfilehash: dfb9dd2703a843b9f09ba1404cd9acfddc25620ff2dc4a00566b4c1582847449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075010"
---
# <a name="recttype-function"></a>Função <Type> Rect

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
| Type      | O tipo de dados usado para armazenar as dimensões do retângulo. Os valores possíveis **são FLOAT** **e UINT32.** |



 

## <a name="parameters"></a>Parâmetros



| Parâmetro | Descrição                                             |
|-----------|---------------------------------------------------------|
| esquerda      | A coordenada X do canto superior esquerdo do retângulo.  |
| top       | A coordenada Y do canto superior esquerdo do retângulo.  |
| direita     | A coordenada X do canto inferior direito do retângulo. |
| parte inferior    | A coordenada Y do canto inferior direito do retângulo. |



 

## <a name="return-value"></a>Valor Retornado

Uma estrutura de retângulo que contém as coordenadas especificadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e Atualização de Plataforma para Windows aplicativos \[ UWP da área de trabalho do Vista \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e Atualização de Plataforma para aplicativos \[ UWP do Windows Server 2008 \|\]<br/> |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





