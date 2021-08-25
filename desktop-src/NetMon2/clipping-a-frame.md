---
description: Você pode especificar que o driver corte os quadros.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Recorte de um quadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9251fc6f8a1c9612a9fa7301ea8948956291ad0d074f90ff2ccbbf3f799bd2b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911256"
---
# <a name="clipping-a-frame"></a>Recorte de um quadro

Você pode especificar que o driver corte os quadros. (Se as outras seções de filtro de captura são omitidas, essa pode ser a única função do filtro de captura). Se o **campo nFrameBytesToCopy** não for zero (0), seu valor especificará quantos bytes de cada quadro recebeu para reter. Se o campo for zero, o quadro inteiro será mantido.

> [!Note]  
> Você pode cortar qualquer quadro que passe as outras partes do filtro de captura definindo **nFrameBytesToCopy**.

 

 

 



