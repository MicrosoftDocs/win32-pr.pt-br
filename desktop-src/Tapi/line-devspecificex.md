---
description: A mensagem de DEVSPECIFICEX de linha TAPI \_ é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Mensagem de LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b65b322b265b6bbd9717a9fc5b3c0eccf46bb3802fef7684a58d2d69645cdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867066"
---
# <a name="line_devspecificex-message"></a>Mensagem de DEVSPECIFICEX de linha \_

A mensagem **de \_ DEVSPECIFICEX de linha** TAPI é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para um dispositivo de linha ou uma chamada. Esse parâmetro é específico do dispositivo.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Específico do dispositivo.

</dd> <dt>

*dwParam2* 
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

A **mensagem \_ DEVSPECIFICEX de linha** é usada por um provedor de serviços em conjunto com a função [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) . Seu significado é específico ao dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




