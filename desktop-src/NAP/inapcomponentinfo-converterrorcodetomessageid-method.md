---
title: Método INapComponentInfo ConvertErrorCodeToMessageId (NapCommon. h)
description: É usado pelo sistema NAP para solicitar que o cliente de integridade Converta um código de erro HRESULT em uma ID de mensagem.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Método ConvertErrorCodeToMessageId NAP
- Método ConvertErrorCodeToMessageId NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método ConvertErrorCodeToMessageId
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
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455880"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a>Método INapComponentInfo:: ConvertErrorCodeToMessageId

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapComponentInfo:: ConvertErrorCodeToMessageId** é usado pelo sistema NAP para solicitar que o cliente de integridade Converta um código de erro HRESULT em uma ID de mensagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ErrorCode* \[ no\]
</dt> <dd>

O [**código de erro**](nap-error-constants.md) do sistema NAP que deve ser convertido em uma **MessageId**.

</dd> <dt>

*msgid* \[ fora\]
</dt> <dd>

Um ponteiro para uma [**MessageId**](nap-datatypes.md) que contém a ID de recurso da cadeia de caracteres localizada correspondente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne um desses códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

O **MessageId** retornado é usado pelo sistema NAP para recuperar uma cadeia de caracteres localizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





