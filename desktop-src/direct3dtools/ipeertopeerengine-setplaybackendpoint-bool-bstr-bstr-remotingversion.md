---
description: Define o endereço do ponto de extremidade usado para se conectar a um mecanismo remoto.
MS-HAID: vspixengine.IPeerToPeerEngine\_SetPlaybackEndpoint\_BOOL\_BSTR\_BSTR\_RemotingVersion
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Método IPeerToPeerEngine::SetPlaybackEndpoint
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D261D2EA-C930-406E-A5E1-CE5E98162399
api_name:
- IPeerToPeerEngine.SetPlaybackEndpoint
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 68a52342f3494b831439764eb74cd16132ec770e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622932"
---
# <a name="span-idvspixengineipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversionspanipeertopeerenginesetplaybackendpoint-method"></a><span id="vspixengine.ipeertopeerengine_setplaybackendpoint_bool_bstr_bstr_remotingversion"></span>Método IPeerToPeerEngine::SetPlaybackEndpoint

Define o endereço do ponto de extremidade usado para se conectar a um mecanismo remoto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPlaybackEndpoint(
   BOOL            bUseAuthentication,
   BSTR            endpoint,
   BSTR            sessionKey,
   RemotingVersion remoteVersion
);
```

## <a name="parameters"></a>Parâmetros

*bUseAuthentication*   
true para usar a autenticação; caso contrário, false.

*Extremidade*   
Uma cadeia de caracteres COM que contém o endereço do ponto de extremidade.

*Sessionkey*   
Uma cadeia de caracteres COM que contém a chave de sessão usada para criptografia.

*remoteVersion*   
Especifica a versão do mecanismo remoto a ser usada.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Confira também

[**IPeerToPeerEngine**](/windows/desktop/direct3dtools/ipeertopeerengine)

 

 
