---
title: Método INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient. h)
description: É usado por clientes de imposição para processar um SoHResponse sempre que eles recebem um blob de dados SoHResponse do servidor de imposição.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Método ProcessSoHResponse NAP
- Método ProcessSoHResponse NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método ProcessSoHResponse
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
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499830"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a>INapEnforcementClientBinding: método rocessSoHResponse de:P

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapEnforcementClientBinding::P rocesssohresponse** é usado pelos clientes de imposição para processar um SoHResponse sempre que eles recebem um blob de dados SoHResponse do servidor de imposição.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*conexão* \[ do no\]
</dt> <dd>

Um ponteiro COM para a interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) da conexão do cliente. O NapAgent não mantém referências ao objeto associado a essa interface após a conclusão dessa chamada de método.

Você deve usar uma conexão estabelecida anteriormente para processar blobs de dados SOHResponse.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | A operação teve êxito.<br/>                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>            | Nenhuma conexão foi criada anteriormente no cliente de imposição. <br/>                                                                                                                                                                                                                                                 |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Erro de permissões, acesso negado.<br/>                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | O limite de recursos do sistema não pôde executar a operação.<br/>                                                                                                                                                                                                                                                                 |
| <dl> <dt>**\_pacote NAP E \_ inválido \_**</dt> </dl>  | Se esse valor for retornado, o cliente de imposição deverá descartar o pacote se o NapAgent retornar um \_ pacote NAP E \_ inválido \_ . Nesse caso, o aplicador deve assumir que o servidor ao qual está se comunicando não é habilitado para NAP e remover a conexão da lista ativa (ou seja, notificar o NapAgent de um estado de conexão).<br/> |
| <dl> <dt>**ID de NAP \_ E não \_ correspondente \_**</dt> </dl>   | Se esse valor for retornado, isso indica que a ID de correlação no pacote de SoH-Response não correspondeu à resposta SoH-Response pendente. Nesse caso, o aplicador deve descartar o pacote e aguardar outro pacote de SoH-Response mais recente.<br/> Isso pode ser causado por uma resposta a uma mensagem de solicitação mais antiga.<br/>        |
| <dl> <dt>**NAP \_ E \_ não \_ inicializado**</dt> </dl> | O imforçador não foi inicializado anteriormente.<br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

O NapAgent consulta o blob de dados SoH-Response do objeto de conexão, processa-o e define a decisão resultante (por exemplo, acesso completo/restrito/etc.) no objeto de conexão.

O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





