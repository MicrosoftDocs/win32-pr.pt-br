---
description: Se as regras de Seleção padrão não atenderem às necessidades do aplicativo, o aplicativo terá a opção de selecionar o terminal manualmente.
ms.assetid: 12d7781e-a27d-4cbe-b7c4-6c0dfef11074
title: Seleção manual de terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6eaa1e0a5b8b53b1037c51b0e628d7a27ece0be65a0f9a7e86e882c722360f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514636"
---
# <a name="manual-terminal-selection"></a>Seleção manual de terminal

Se as regras de Seleção padrão não atenderem às necessidades do aplicativo, o aplicativo terá a opção de selecionar o terminal como sempre tem: ou seja, ele poderá usar [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) para enumerar os fluxos presentes na chamada e selecionar o terminal nos fluxos apropriados (ou, no caso de terminais multitrack, criar faixas para os fluxos e selecionar faixas criadas nos fluxos).

 

 
