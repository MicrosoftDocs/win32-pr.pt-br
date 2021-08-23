---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320572322d7a28b52693c80eb918ebf78fcb50083e012e35c65df3a7bffdf0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976396"
---
# <a name="iagentcharacterplay"></a>IAgentCharacter::P deite

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Reproduz a animação especificada.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida. Quando a função retorna, *pdwReqID* contém a ID da solicitação.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*
</dt> <dd>

O nome de uma animação.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID de solicitação de:P de direcionamento de **IAgentCharacter:** .

</dd> </dl>

O nome de uma animação é definido quando o caractere é compilado com o editor de caracteres do Microsoft Agent. Antes de reproduzir a animação especificada, o servidor tenta reproduzir a animação de **retorno** para a animação anterior (se uma tiver sido atribuída).

Quando os dados de animação de um caractere são armazenados no computador local do usuário, você pode usar o método **IAgentCharacter::P deite** e especificar o nome da animação. Ao usar o protocolo HTTP para acessar dados de animação, use o método [**Prepare**](iagentcharacter--prepare.md) para garantir a disponibilidade da animação antes de chamar esse método.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::P reparênteses**](iagentcharacter--prepare.md)


 

 




