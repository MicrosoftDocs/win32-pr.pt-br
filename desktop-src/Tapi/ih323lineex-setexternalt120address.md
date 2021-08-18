---
description: O método SetExternalT120Address é chamado por um aplicativo para configurar um endereço T.120 externo para troca de dados.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: Método IH323LineEx::SetExternalT120Address (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8889887c396c427c28ac2906206b3e3cbbcb102daa937720b6b879472b47bbdc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992086"
---
# <a name="ih323lineexsetexternalt120address-method"></a>Método IH323LineEx::SetExternalT120Address

\[**SetExternalT120Address** não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método SetExternalT120Address** é chamado por um aplicativo para configurar um endereço T.120 externo para troca de dados. A funcionalidade T.120 será anunciada durante a negociação H.245 e o endereço será usado na confirmação de canal lógico aberto para que o outro ponto de extremidade possa configurar sessões T.120 com o serviço escutando nesse endereço. Se essa função não for chamada, o provedor de serviços H.323 não anunciará a funcionalidade T.120.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnable* \[ Em\]
</dt> <dd>

**TRUE** para habilitar a funcionalidade T.120; **FALSE** para desabilitar a funcionalidade T.120.

</dd> <dt>

*dwIP* \[ Em\]
</dt> <dd>

**DWORD** que contém o endereço IP na ordem de byte do host do serviço T.120 externo.

</dd> <dt>

*wPort* \[ Em\]
</dt> <dd>

**WORD** que contém a porta do serviço T.120 externo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                          | Descrição                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




