---
description: O comportamento padrão para o controle InkEdit é reconhecer e converter tinta em texto após um breve tempo de expiração.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Exibindo tinta como tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de038df5c1b7e43f90ea02edc166039d606fe56761c96a47508714fd94ed6530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709466"
---
# <a name="displaying-ink-as-ink"></a>Exibindo tinta como tinta

O comportamento padrão para o [controle InkEdit](inkedit-control-reference.md) é reconhecer e converter tinta em texto após um breve tempo de expiração. Como o controle é uma superclasse [de RichEdit](../controls/rich-edit-controls.md), também é possível inserir e exibir tinta dentro do controle. Cada palavra é inserida no controle como um [**objeto InkDisp.**](inkdisp-class.md) O **objeto InkDisp** contém a tinta e suas alternativas de reconhecimento.

Quando inserida, a tinta é dimensionada para o tamanho atual da fonte e outras propriedades de ambiente, como itálico ou negrito, são aplicadas. Se o usuário optar por editar o texto de um [**objeto InkDisp,**](inkdisp-class.md) primeiro ele deverá converter a tinta em texto.

> [!Note]  
> Todos os dados alternativos de tinta e reconhecimento são perdidos durante a conversão.

 

Esse recurso está disponível somente em computadores que executem o Microsoft Windows XP Tablet PC Edition, Windows Vista ou posterior.

 

 
