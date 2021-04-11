---
title: Estrutura EapHostPeerNapInfo (Eaphostpeerapis. h)
description: Contém as informações de NAP (proteção de acesso à rede) em um suplicante de EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Estrutura EapHostPeerNapInfo EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009684"
---
# <a name="eaphostpeernapinfo-structure"></a>Estrutura EapHostPeerNapInfo

A estrutura **EapHostPeerNapInfo** contém as informações de NAP (proteção de acesso à rede) em um suplicante de EAP.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a>Membros

<dl> <dt>

**isolamentostate**
</dt> <dd>

Uma estrutura de [**\_ estado de isolamento**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) que especifica o estado de isolamento NAP de um computador. O estado de isolamento determina o nível de acesso à rede concedido.

</dd> <dt>

**experiênciatime**
</dt> <dd>

Uma estrutura de **experiênciatime** que especifica o tempo necessário para a conexão sair da quarentena após a qual a conexão será descartada. Uma estrutura de modo de **experiência** é idêntica a uma estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .

</dd> <dt>

**stringCorrelationIdLength**
</dt> <dd>

O comprimento, em bytes, do [STRINGCORRELATIONID](/windows/desktop/NAP/nap-datatypes) NAP que segue essa estrutura.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura **EapHostPeerNapInfo** precede a [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) de NAP do tipo de dados **WCHAR** no fluxo de bytes RPC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Eaphostpeerapis. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do suplicante EAPHost](eap-host-supplicant-structures.md)
</dt> <dt>

[**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**EapHostPeerMethodAuthParams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

