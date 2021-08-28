---
description: A mensagem TAPI LINE DEVSPECIFIC é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma \_ linha, endereço ou chamada. O significado da mensagem e a interpretação dos parâmetros são específicos do dispositivo.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: LINE_DEVSPECIFIC mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca1ba410ac3127ff917965e8eda7c579be68dab5150c6dcae63a1930a98d265
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975666"
---
# <a name="line_devspecific-message"></a>Mensagem LINE \_ DEVSPECIFIC

A mensagem TAPI **LINE \_ DEVSPECIFIC** é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e a interpretação dos parâmetros são específicos do dispositivo.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um alça para um dispositivo de linha ou uma chamada. Isso é específico do dispositivo.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem LINE \_ DEVSPECIFIC** é usada por um provedor de serviços em conjunto com a [**função lineDevSpecific.**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) Seu significado é específico do dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




