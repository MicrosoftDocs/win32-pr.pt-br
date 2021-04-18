---
description: A mensagem de DEVSPECIFICFEATURE de linha TAPI \_ é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: Mensagem de LINE_DEVSPECIFICFEATURE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788057"
---
# <a name="line_devspecificfeature-message"></a>Mensagem de DEVSPECIFICFEATURE de linha \_

A mensagem **de \_ DEVSPECIFICFEATURE de linha** TAPI é enviada para notificar o aplicativo sobre eventos específicos do dispositivo que ocorrem em uma linha, endereço ou chamada. O significado da mensagem e da interpretação dos parâmetros são específicos do dispositivo.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para um dispositivo de linha ou uma chamada. Este é um dispositivo específico.

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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem \_ DEVSPECIFICFEATURE de linha** é usada por um provedor de serviços em conjunto com a função [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) . Seu significado é específico ao dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




