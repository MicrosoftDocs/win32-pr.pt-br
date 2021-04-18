---
description: Não há suporte para a função RKeyOpenKeyService.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Função RKeyOpenKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810508"
---
# <a name="rkeyopenkeyservice-function"></a>Função RKeyOpenKeyService

Não há suporte para a função **RKeyOpenKeyService** .

**Windows Server 2003:** A função **RKeyOpenKeyService** estabelece uma conexão com um computador remoto e abre um identificador de serviço de chave. O identificador de serviço de chave pode ser usado subsequentemente pela função [**RKeyPFXInstall**](rkeypfxinstall.md) . Observe que esse comportamento foi alterado com o Windows Server 2003 com Service Pack 1 (SP1).

## <a name="syntax"></a>Sintaxe


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszMachineName* \[ no\]
</dt> <dd>

Ponteiro longo para uma cadeia de caracteres terminada em nulo que representa o computador em que o identificador de serviço de chave será aberto.

</dd> <dt>

*OwnerType* \[ no\]
</dt> <dd>

[**KEYSVC \_ Digite**](keysvc-type.md) o valor que representa o tipo de chave. O único valor com suporte é **KeySvcMachine**.

</dd> <dt>

*pwszOwnerName* \[ no\]
</dt> <dd>

Reservado. Defina esse valor como **NULL**.

</dd> <dt>

*pAuthentication* \[ no\]
</dt> <dd>

Um ponteiro para um **void** que representa as configurações de autenticação. Esse ponteiro pode apontar para um valor de zero ou o valor a seguir.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <dt>**RKEYSVC \_ CONECTAR \_ \_ somente segurança**</dt><dt></dt> </dl> | O cliente requer autenticação mútua. Se esse valor for especificado, haverá falha no fallback para NTLM.<br/> |



 

</dd> <dt>

*preservado* \[ entrada, saída\]
</dt> <dd>

Reservado. Defina esse valor como **NULL**.

</dd> <dt>

*phKeySvcCli* \[ fora\]
</dt> <dd>

Um ponteiro para um [**\_ identificador de KEYSVCC**](keysvcc-handle.md) que recebe o identificador de serviço de chave aberto. Quando você terminar de usar o identificador, libere o recurso chamando a função [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será S \_ OK.

Se a função falhar, o valor de retorno será um **ULONG** que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




