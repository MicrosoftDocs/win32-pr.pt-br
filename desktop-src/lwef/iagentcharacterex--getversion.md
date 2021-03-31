---
title: GetVersion do IAgentCharacterEx
description: GetVersion do IAgentCharacterEx
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005331"
---
# <a name="iagentcharacterexgetversion"></a>IAgentCharacterEx:: GetVersion

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

Recupera o número de versão do conjunto de animações padrão de caracteres.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*
</dt> <dd>

Endereço de uma variável que recebe a versão principal.

</dd> <dt>

<span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*
</dt> <dd>

Endereço de uma variável que recebe a versão secundária.

</dd> </dl>

O número de versão do conjunto de animações padrão é definido automaticamente quando você o cria com o editor de caracteres do Microsoft Agent.

 

 




