---
title: Método IMsTscAxEvents OnReceivedTSPublicKey
description: Chamado durante a sequência de conexão quando o cliente recupera a chave pública do servidor. Esse evento só será chamado se a propriedade NotifyTSPublicKey for VARIANT \_ true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnReceivedTSPublicKey
- Método OnReceivedTSPublicKey Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnReceivedTSPublicKey
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73f2b12b59cbe8e6b7c5f8e614e2aed047d4f467117fa211839521fedc7f333b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009476"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a>Método IMsTscAxEvents:: OnReceivedTSPublicKey

Chamado durante a sequência de conexão quando o cliente recupera a chave pública do servidor. Esse evento só será chamado se a propriedade **NotifyTSPublicKey** for **Variant \_ true**. Isso ocorre após a [**desconexão**](imstscaxevents-onconnecting.md), mas antes de OnAuthenticationWarningDisplayed [**e onconnected**](imstscaxevents-onconnected.md). [](imstscaxevents-onauthenticationwarningdisplayed.md)

## <a name="syntax"></a>Sintaxe


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PublicKey* \[ no\]
</dt> <dd>

Contém a chave pública do computador remoto.

</dd> <dt>

*pfContinueLogon* \[ fora\]
</dt> <dd>

Um ponteiro para uma **variável \_ bool variante** que recebe se o processo de logon deve continuar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows servidor 2008, Windows server 2008 com SP1<br/>                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





