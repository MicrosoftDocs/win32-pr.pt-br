---
title: Função de tipo Point2 (D2d1helper.h)
description: Cria um ponto que armazena suas coordenadas usando o tipo de dados especificado.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Função de tipo Point2 Direct2D
topic_type:
- apiref
api_name:
- Point2 Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79208c0e68736ae91d623622c13bbeb624ab760
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887196"
---
# <a name="point2lttypegt-function"></a>Função de tipo &lt; Point2 &gt;

Cria um ponto que armazena suas coordenadas usando o tipo de dados especificado.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Point Point2(
  Type x,
  Type y
);
```

## <a name="template-parameters"></a>Parâmetros de modelo



| Parâmetro | Descrição                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------|
| Type      | O tipo de dados usado para armazenar a coordenada x e a coordenada y do ponto. Os valores possíveis são FLOAT e UINT32. |



 

## <a name="parameters"></a>Parâmetros



| Parâmetro | Descrição                    |
|-----------|--------------------------------|
| x         | A coordenada X do ponto. |
| a         | A coordenada Y do ponto. |



 

## <a name="return-value"></a>Valor Retornado

Um ponto que contém a coordenada x e a coordenada y especificadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e Atualização de Plataforma para Windows aplicativos \[ UWP da área de trabalho do Vista \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e Atualização de Plataforma para aplicativos \[ UWP do Windows Server 2008 \|\]<br/> |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





