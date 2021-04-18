---
description: Você pode especificar que o driver corte os quadros.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Recortando um quadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811823"
---
# <a name="clipping-a-frame"></a>Recortando um quadro

Você pode especificar que o driver corte os quadros. (Se as outras seções de filtro de captura forem omitidas, essa poderá ser a única função do seu filtro de captura). Se o campo **nFrameBytesToCopy** não for zero (0), seu valor especificará quantos bytes de cada quadro receberão para reter. Se o campo for zero, o quadro inteiro será retido.

> [!Note]  
> Você pode cortar qualquer quadro que passe as outras partes do filtro de captura definindo **nFrameBytesToCopy**.

 

 

 



