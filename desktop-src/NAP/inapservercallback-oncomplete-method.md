---
title: Método OnComplete do INapServerCallback (NapSystemHealthValidator. h)
description: Usado por SHVs para sinalizar a conclusão da solicitação assíncrona.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Método OnComplete NAP
- Método OnComplete NAP, interface INapServerCallback
- Interface INapServerCallback NAP, método OnComplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456022"
---
# <a name="inapservercallbackoncomplete-method"></a>Método INapServerCallback:: OnComplete

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapServerCallback:: OnComplete** é usado por SHVs para sinalizar a conclusão da solicitação assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*solicitação* \[ do no\]
</dt> <dd>

Um ponteiro para um objeto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que representa uma solicitação de validação.

</dd> <dt>

*ErrorCode* \[ no\]
</dt> <dd>

Um [**código de erro NAP**](nap-error-constants.md) que indica o motivo pelo qual a validação não pôde ser executada.

> [!Note]  
> Normalmente, o valor de retorno do método [**INapSystemHealthValidationRequest:: SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) é passado para esse parâmetro. No entanto, se **SetSoHResponse** não puder ser chamado devido a uma falha de reprocessamento, o valor retornado pelo comando com falha será passado.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operação bem-sucedida.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

Os validadores devem retornar S \_ OK se a validação de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) puder ser concluída, independentemente de o **SoHRequest** ter passado a verificação de integridade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| parâmetro<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapServerCallback**](inapservercallback.md)
</dt> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





