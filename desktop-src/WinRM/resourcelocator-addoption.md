---
title: Método ResourceLocator.AddOption (WSManDisp.h)
description: Adiciona dados adicionais necessários para processar a solicitação. Por exemplo, alguns provedores WMI podem exigir um objeto IWbemContext ou SWbemNamedValueSet com informações específicas do provedor.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Método AddOption Windows Gerenciamento Remoto
- Método AddOption Windows gerenciamento remoto, objeto ResourceLocator
- Objeto ResourceLocator Windows Gerenciamento Remoto, Método AddOption
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c03e587c4884e6d9efc3b98bdd7b41b4204a783e153d9e59a400a4e4bc02a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112961"
---
# <a name="resourcelocatoraddoption-method"></a>Método ResourceLocator.AddOption

Adiciona dados adicionais necessários para processar a solicitação. Por exemplo, alguns provedores WMI podem exigir um [**objeto IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) com informações específicas do provedor. Você pode fornecer um [**objeto ResourceLocator**](resourcelocator.md) em vez [](session.md) de especificar um URI de recurso em operações de objeto session, como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)ou [**Session.Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxe


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OptionName* \[ Em\]
</dt> <dd>

O nome (chave) do objeto de dados opcional.

</dd> <dt>

*OptionValue* \[ Em\]
</dt> <dd>

Um valor fornecido para o objeto de dados opcional.

</dd> <dt>

*mustComply* \[ Em\]
</dt> <dd>

Um sinalizador que indica que a opção deve ser processada. O padrão é **False** (0).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

**IWSManResourceLocator::AddOption** é o método C++ correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

