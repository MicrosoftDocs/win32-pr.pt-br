---
title: Método INapComponentInfo ConvertErrorCodeToMessageId (NapCommon.h)
description: É usado pelo sistema NAP para solicitar que o cliente de saúde converta um código de erro HRESULT em uma ID de mensagem.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Método NAP ConvertErrorCodeToMessageId
- Método NAP ConvertErrorCodeToMessageId, interface INapComponentInfo
- Interface INapComponentInfo NAP, método ConvertErrorCodeToMessageId
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c670585674713d114f6505a0c3211d599663545f6b06a40669f7fba8b7eddf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621725"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>Método INapComponentInfo::ConvertErrorCodeToMessageId

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapComponentInfo::ConvertErrorCodeToMessageId** é usado pelo sistema NAP para solicitar que o cliente de saúde converta um código de erro HRESULT em uma ID de mensagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*errorCode* \[ Em\]
</dt> <dd>

O [**código de**](nap-error-constants.md) erro do sistema NAP que deve ser convertido em uma **MessageId.**

</dd> <dt>

*msgId* \[ out\]
</dt> <dd>

Um ponteiro para uma [**MessageId**](nap-datatypes.md) que contém a ID do recurso da cadeia de caracteres localizada correspondente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar um desses códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

A **MessageId retornada** é usada pelo sistema NAP para recuperar uma cadeia de caracteres localizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





