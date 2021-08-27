---
description: A mensagem TAPI PHONE \_ CREATE é enviada para informar os aplicativos sobre a criação de um novo dispositivo de telefone.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: PHONE_CREATE mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18633ca9f3d45e08c3e2e054d51261dabe6494f42055567a5a68707408f94d5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072906"
---
# <a name="phone_create-message"></a>Mensagem PHONE \_ CREATE

A mensagem TAPI **PHONE \_ CREATE** é enviada para informar os aplicativos sobre a criação de um novo dispositivo de telefone.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

O *hDeviceID* do dispositivo recém-criado.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Não utilizado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Os aplicativos que negociavam a API versão 1.3 são enviados uma mensagem [**PHONE \_ STATE**](phone-state.md) especificando PHONESTATE REINIT, o que exige que eles desliguem o uso da API e liguem \_ para [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) novamente para obter o novo número de dispositivos. No entanto, a TAPI versão 1.4 e superior não exigem que todos os aplicativos desliguem antes de permitir que os aplicativos reinicializam; A reinicialização pode ocorrer imediatamente quando um novo dispositivo é criado.

Aplicativos que suportam TAPI versão 1.4 ou posterior são enviados uma **mensagem PHONE \_ CREATE.** Isso informa a eles sobre a existência do novo dispositivo e seu novo identificador de dispositivo. Em seguida, o aplicativo pode escolher se quer ou não tentar trabalhar com o novo dispositivo em sua totalidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ESTADO \_ DO TELEFONE**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**Phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




