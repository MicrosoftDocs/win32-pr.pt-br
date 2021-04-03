---
title: Sinalizadores de prioridade
description: O sinalizador de prioridade abre um objeto de armazenamento no modo de prioridade.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Sinalizadores de prioridade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006201"
---
# <a name="priority-flags"></a>Sinalizadores de prioridade

O sinalizador de prioridade abre um objeto de armazenamento no modo de prioridade. Quando ele abre um objeto, um aplicativo geralmente funciona a partir de uma cópia de instantâneo porque outros aplicativos também podem estar usando o objeto ao mesmo tempo. No entanto, ao abrir um objeto de armazenamento no modo de prioridade, o aplicativo tem direitos exclusivos para confirmar as alterações no objeto.

O modo de prioridade permite que um aplicativo Leia alguns fluxos do armazenamento antes de abrir o objeto em um modo que exige que o sistema faça uma cópia de instantâneo. Como o aplicativo tem acesso exclusivo, ele não precisa fazer uma cópia de instantâneo do objeto. Quando o aplicativo abre o objeto subsequentemente em um modo em que uma cópia de instantâneo é necessária, o aplicativo pode excluir os fluxos já lidos do instantâneo, reduzindo assim a sobrecarga de abrir o objeto.

Como outros aplicativos não podem confirmar alterações em um objeto enquanto ele está aberto no modo de prioridade, os aplicativos devem manter o objeto nesse modo pelo menor tempo possível.

 

 




