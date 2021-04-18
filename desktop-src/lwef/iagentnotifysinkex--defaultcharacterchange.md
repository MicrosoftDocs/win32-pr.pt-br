---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105814075"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a>IAgentNotifySinkEx::D efaultCharacterChange

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

Notifica um aplicativo cliente quando o caractere padrão é alterado.

-   Sem valor de retorno.

<dl> <dt>

<span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*
</dt> <dd>

O identificador exclusivo do caractere.

</dd> </dl>

Quando o usuário altera o caractere atribuído como o caractere padrão do usuário, o servidor envia esse evento aos clientes que carregaram o caractere padrão. O evento retorna o GUID (identificador exclusivo) do caractere formatado com chaves e traços, que é definido quando o caractere é compilado com o editor de caracteres do Microsoft Agent.

Quando o novo caractere é exibido, ele assume o mesmo tamanho que qualquer instância já carregada do caractere ou o caractere padrão anterior (nessa ordem).

## <a name="see-also"></a>Consulte Também

[**IAgent:: Load**](iagent--load.md)


 

 




