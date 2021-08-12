---
title: Método INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient.h)
description: É usado pelos clientes de imposição para processar um SoHResponse sempre que recebem um blob de dados SoHResponse do servidor de imposição.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Nap do método ProcessSoHResponse
- Método ProcessSoHResponse NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP , método ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cffd2caeaf3a39bd5c28b4850fc560dc9567a3552aad88929581efd2729acce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621705"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>Método INapEnforcementClientBinding::P rocessSoHResponse

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientBinding::P rocessSoHResponse** é usado pelos clientes de imposição para processar um SoHResponse sempre que recebem um blob de dados SoHResponse do servidor de imposição.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*conexão* \[ Em\]
</dt> <dd>

Um ponteiro COM para a interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) da conexão do cliente. O NapAgent não mantém referências ao objeto associado a essa interface depois que essa chamada de método é concluída.

Você deve usar uma conexão estabelecida anteriormente para processar blobs de dados SOHResponse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos do COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | A operação teve êxito.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Nenhuma conexão foi criada anteriormente no cliente de imposição. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite de recursos do sistema, não foi possível executar a operação.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**NAP \_ E \_ PACOTE \_ INVÁLIDO**</dt> </dl>  | Se esse valor for retornado, o cliente de imposição deverá soltar o pacote se NapAgent retornar NAP \_ E \_ INVALID \_ PACKET. Nesse caso, o executor deve assumir que o servidor com o que está se comunicando não está habilitado para NAP e remover a conexão da lista ativa (ou seja, notificar o NapAgent de um estado de conexão para baixo).<br/> |
| <dl> <dt>**\_NAP E \_ \_ ID INCOMPATIBILIDADE**</dt> </dl>   | Se esse valor for retornado, isso indicará que a ID de correlação no pacote SoH-Response não corresponder ao SoH-Response pendente. Nesse caso, o executor deve soltar o pacote e aguardar outro pacote SoH-Response mais recente.<br/> Isso pode ser causado por uma resposta a uma mensagem de solicitação mais antiga.<br/>        |
| <dl> <dt>**NAP \_ E \_ NÃO \_ INICIALIZADO**</dt> </dl> | O executor não foi inicializado anteriormente.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

O NapAgent consulta o SoH-Response blob de dados do objeto de conexão, processa-o e define a decisão resultante (por exemplo, acesso completo/restrito/etc) no objeto de conexão.

O cliente de imposição deve chamar o método [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





