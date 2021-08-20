---
title: Método GetLocalizedString INapComponentInfo (NapCommon.h)
description: É usado pelo sistema NAP para obter cadeias de caracteres localizadas.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- NAP do método GetLocalizedString
- Método GetLocalizedString NAP, interface INapComponentInfo
- Nap da interface INapComponentInfo, método GetLocalizedString
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be55595bf6c5af6e435d9c53c9b473a721005699da494319ba55eaa828da2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134359"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a>Método INapComponentInfo::GetLocalizedString

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapComponentInfo::GetLocalizedString** é usado pelo sistema NAP para obter cadeias de caracteres localizadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*msgId* \[ Em\]
</dt> <dd>

Uma [**MessageId**](nap-datatypes.md) que contém a ID do recurso da cadeia de caracteres a ser localizada.

</dd> <dt>

*cadeia de caracteres* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para [**um CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a versão localizada da mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar um desses códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite de recursos do sistema, não foi possível executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

As cadeias de caracteres devem ser localizadas de acordo com a ID de idioma do thread de chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





