---
title: D1102 Muitas alças abertas
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: Um grande número de interfaces não lançados foi encontrado. Atualmente, há interfaces não lançados alocadas por essa DLL.
keywords:
- D1102 Muitas alças abertas Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: baaa4c46850919aed50897583bfa68c9003bcf496ad884c68cfb57d3e8a90147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666347"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: muitos alças abertas

Um grande número de interfaces não lançados foi encontrado. Atualmente, há \[ *interfaces* \] de número não lançado alocadas por essa DLL.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*Número*
</dt> <dd>

O número de interfaces não lançados alocadas por essa DLL.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nível de erro | Aviso |



 

## <a name="possible-causes"></a>Possíveis causas

Um grande número de recursos foi criado. Embora Direct2D não tenha limite superior no número de recursos disponíveis (exceto memória), a camada de depuração emite essa mensagem informativa quando encontra 1001 objetos ao vivo, 2001 objetos ativos ou 3001 objetos ativos etc. porque isso pode indicar uma perda no aplicativo.

 

 




