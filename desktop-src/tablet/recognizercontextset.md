---
description: Testa se o objeto InkDivider pode usar a classe InkRecognizerContext para analisar palavras.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: Função RecognizerContextSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: fee6fa3f9f9743f048cab4d9bee5af3fa9215ca903227acd0aa67cb68037550d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934706"
---
# <a name="recognizercontextset-function"></a>Função RecognizerContextSet

Testa se o [**objeto InkDivider**](inkdivider-class.md) pode usar a [**classe InkRecognizerContext**](inkrecognizercontext-class.md) para analisar palavras.

Essa função não se destina a ser usada pelo código do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDivider* \[ Em\]
</dt> <dd>

Um identificador para o [**objeto InkDivider.**](inkdivider-class.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função pode retornar um desses valores.



| Código de retorno                                                                                  | Descrição                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A função foi bem-sucedida.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O *parâmetro pDivider* é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Biblioteca<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




