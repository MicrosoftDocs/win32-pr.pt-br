---
title: Função size type (D2d1helper.h)
description: Cria uma estrutura de tamanho que armazena sua largura e altura usando o tipo de dados especificado.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Função size type Direct2D
topic_type:
- apiref
api_name:
- Size Type Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf2bac3b43cf083d4f2d3588fed41d55380a435cc10c56cdfdb5cae1929d12c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292776"
---
# <a name="sizetype-function"></a>Função <Type> Size

Cria uma estrutura de tamanho que armazena sua largura e altura usando o tipo de dados especificado.

``` syntax
template<typename Type>
typename TypeTraits<Type>::Size Size(
  Type width,
  Type height
);
```

## <a name="template-parameters"></a>Parâmetros de modelo



| Parâmetro | Descrição                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------|
| Type      | O tipo de dados usado para armazenar a largura e a altura do tamanho. Os valores possíveis são FLOAT e UINT32. |



 

## <a name="parameters"></a>Parâmetros



| Parâmetro | Descrição        |
|-----------|--------------------|
| width     | A largura do tamanho.  |
| altura    | A altura do tamanho. |



 

## <a name="return-value"></a>Valor Retornado

Um tamanho que contém a largura e a altura especificadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e Atualização de Plataforma para Windows aplicativos \[ UWP da área de trabalho do Vista \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e Atualização de Plataforma para aplicativos \[ UWP do Windows Server 2008 \|\]<br/> |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>D2d1helper.h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





