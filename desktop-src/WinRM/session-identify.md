---
title: Método Session. Identify (WSManDisp. h)
description: Consulta um computador remoto para determinar se ele dá suporte ao protocolo de WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método de identificação
- Gerenciamento Remoto do Windows método de identificação, objeto de sessão
- Gerenciamento Remoto do Windows de objeto de sessão, método Identify
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812095"
---
# <a name="sessionidentify-method"></a>Método Session. Identify

O método **Session. Identify** consulta um computador remoto para determinar se ele dá suporte ao protocolo WS-Management. Para obter mais informações, consulte [detectando se um computador remoto dá suporte ao protocolo WS-Management](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).

## <a name="syntax"></a>Sintaxe


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de em, opcional\]
</dt> <dd>

Para enviar a solicitação no modo autenticado, use a constante de autenticação da enumeração **WSManSessionFlags** . Para enviar em modo não autenticado, use **WSManFlagUseNoAuthentication**. Para obter mais informações, consulte [**constantes de autenticação**](authentication-constants.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma cadeia de caracteres XML que especifica a versão do protocolo WS-Management, o fornecedor do sistema operacional e, se a solicitação foi enviada autenticada, a versão do sistema operacional.

## <a name="remarks"></a>Comentários

**Session. Identify** é baseado na operação de [protocolo WS-Management](ws-management-protocol.md) definida como wsmanIdentity. Isso é especificado no pacote SOAP da seguinte maneira:


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir envia uma solicitação de identificação não autenticada para o computador remoto chamado Remote no mesmo domínio.


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Session**](session.md)
</dt> <dt>

[**IWSManSession:: identificar**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

 





