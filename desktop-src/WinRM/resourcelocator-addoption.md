---
title: Método ResourceLocator. AddOption (WSManDisp. h)
description: Adiciona dados adicionais necessários para processar a solicitação. Por exemplo, alguns provedores WMI podem exigir um objeto IWbemContext ou SWbemNamedValueSet com informações específicas do provedor.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Método AddOption Gerenciamento Remoto do Windows
- Método AddOption Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, método AddOption
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
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009017"
---
# <a name="resourcelocatoraddoption-method"></a>Método ResourceLocator. AddOption

Adiciona dados adicionais necessários para processar a solicitação. Por exemplo, alguns provedores WMI podem exigir um objeto [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) com informações específicas do provedor. Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).

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

*OptionName* \[ no\]
</dt> <dd>

O nome (chave) do objeto de dados opcional.

</dd> <dt>

*Opçãovalue* \[ no\]
</dt> <dd>

Um valor fornecido para o objeto de dados opcional.

</dd> <dt>

*mustComply* \[ no\]
</dt> <dd>

Um sinalizador que indica que a opção deve ser processada. O padrão é **false** (0).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

**IWSManResourceLocator:: AddOption** é o método C++ correspondente.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

