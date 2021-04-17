---
description: O comportamento padrão para o controle InkEdit é reconhecer e converter a tinta em texto depois que um tempo limite curto expirar.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Exibindo tinta como tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770590"
---
# <a name="displaying-ink-as-ink"></a>Exibindo tinta como tinta

O comportamento padrão para o controle [InkEdit](inkedit-control-reference.md) é reconhecer e converter a tinta em texto depois que um tempo limite curto expirar. Como o controle é uma superclasse de [RichEdit](../controls/rich-edit-controls.md), também é possível inserir e exibir tinta dentro do controle. Cada palavra é inserida no controle como um objeto [**InkDisp**](inkdisp-class.md) . O objeto **InkDisp** contém a tinta e suas alternativas de reconhecimento.

Quando inserido, a tinta é dimensionada para o tamanho da fonte atual e outras propriedades de ambiente, como itálico ou negrito, são aplicadas. Se o usuário optar por editar o texto de um objeto [**InkDisp**](inkdisp-class.md) , ele deverá primeiro converter a tinta em texto.

> [!Note]  
> Todos os dados alternativos de reconhecimento e tinta são perdidos durante a conversão.

 

Esse recurso está disponível somente em computadores que executam o Microsoft Windows XP Tablet PC Edition, Windows Vista ou posterior.

 

 
