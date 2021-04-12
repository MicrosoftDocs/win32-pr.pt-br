---
title: Função de tipo de tamanho (D2d1helper. h)
description: Cria uma estrutura de tamanho que armazena sua largura e altura usando o tipo de dados especificado.
ms.assetid: 9f7e37a3-440e-40c0-a527-9fcbd207dce8
keywords:
- Função de tipo de tamanho Direct2D
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
ms.openlocfilehash: a300ab0ce7da57440516733459f703379cf5a943
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454993"
---
# <a name="sizetype-function"></a><Type>Função size

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
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>D2d1helper. h</dt> </dl>                                                  |
| Biblioteca<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

 





