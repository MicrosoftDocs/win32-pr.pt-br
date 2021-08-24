---
description: As constantes a seguir podem ser retornadas como erros.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Constantes de RND_ (Rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ed1b55b0ed18215fb17e27504c309c67b0cea3351acea6cffadc4b3ff31c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773366"
---
# <a name="rnd_-constants"></a>Constantes de RND \_

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

As constantes a seguir podem ser retornadas como erros.

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**\_hora inválida do Rnd \_**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



O valor de hora inserido não é válido.


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**\_ \_ nome do servidor nulo do Rnd \_**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



O nome do servidor é **nulo**, provavelmente porque [**ITConferenceBlob:: init**](itconferenceblob-init.md) não foi executado ou não foi bem sucedido.


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**o RND \_ já \_ está conectado**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



o método [**ITDirectory:: Conexão**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) foi chamado, mas já existe uma conexão.


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ não \_ conectado**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



o método [**ITDirectory:: Conexão**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) não foi chamado ou falhou.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                               |
| Cabeçalho<br/>       | <dl> <dt>Rnderr. h</dt> </dl> |



 

 




