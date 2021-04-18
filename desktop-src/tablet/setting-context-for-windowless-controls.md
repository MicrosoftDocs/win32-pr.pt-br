---
description: Controles sem janela podem chamar a função SetInputScope sempre que o foco é movido entre os elementos do controle sem janela; no entanto, isso não é recomendado por motivos de desempenho.
ms.assetid: 616ffe1a-3788-4a99-bbfa-6cbaf45b93b7
title: Configurando contexto para controles sem janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9165b76bfa5cfb6e8d8d2c0b3593e2f42d923fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766557"
---
# <a name="setting-context-for-windowless-controls"></a>Configurando contexto para controles sem janela

Controles sem janela podem chamar a função [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) sempre que o foco é movido entre os elementos do controle sem janela; no entanto, isso não é recomendado por motivos de desempenho.

 

 
