---
title: Método INapEnforcementClientConnection SetSoHRequest (NapEnforcementClient. h)
description: Define a solicitação SoH.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Método SetSoHRequest NAP
- Método SetSoHRequest NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, método SetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2d2d3a4574b086d49cba7d9c0afda72cf62621dbed37add8550a7ae2f93cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799630"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a>Método INapEnforcementClientConnection:: SetSoHRequest

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientConnection:: SetSoHRequest** define a solicitação soh-Request.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sohRequest* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) exclusiva, que é um blob de dados opaco para o aplicador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | O pacote SoH é válido.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Isso é definido pelo NapAgent e consultado pelos imforçadores para envio na conexão.

Um pacote SoH de comprimento de byte zero é inválido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





