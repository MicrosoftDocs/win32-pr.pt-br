---
description: Um processo pode chamar WSPCloseSocket em um soquete duplicado e o descritor ficará desalocado. No entanto, o soquete subjacente permanecerá aberto até que WSPCloseSocket seja chamado no último descritor restante.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Contagem de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8cd281363636cc2022725b4921d3b2d2b300e7262173e157a2be1610f6af0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996656"
---
# <a name="reference-counting"></a>Contagem de referência

Um processo pode chamar [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) em um soquete duplicado e o descritor ficará desalocado. No entanto, o soquete subjacente permanecerá aberto até que **WSPCloseSocket** seja chamado no último descritor restante.

 

 
