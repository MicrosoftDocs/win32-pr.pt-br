---
title: D1102 um número excessivo de identificadores abertos
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Um grande número de interfaces não lançadas foi encontrado. Atualmente, há interfaces não lançadas alocadas por essa DLL.
keywords:
- D1102 um número excessivo de identificadores abertos Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548681"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: muitos identificadores abertos

Um grande número de interfaces não lançadas foi encontrado. Atualmente, há um \[ *número* \] de interfaces não lançadas alocadas por essa dll.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*automática*
</dt> <dd>

O número de interfaces não lançadas alocadas por essa DLL.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nível de erro | Aviso |



 

## <a name="possible-causes"></a>Possíveis causas

Um grande número de recursos foi criado. Embora Direct2D não tenha limite superior no número de recursos disponíveis (exceto memória), a camada de depuração emite essa mensagem informativa quando encontra 1001 objetos dinâmicos, 2001 objetos dinâmicos ou 3001 objetos dinâmicos etc, porque isso pode indicar um vazamento no aplicativo.

 

 




