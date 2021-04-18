---
title: Função de tipo Point2 (D2d1helper. h)
description: Cria um ponto que armazena suas coordenadas usando o tipo de dados especificado.
ms.assetid: 59a631ae-d70e-4ee2-9546-2d19da40aa9b
keywords:
- Função de tipo point2 Direct2D
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
ms.openlocfilehash: f614f49077ed198c5e85d17b9ee3c84a5e300670
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751289"
---
# <a name="point2type-function"></a><Type>Função point2

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

Um ponto que contém a coordenada x e a coordenada y especificados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





