---
title: Método ResourceLocator. addseletor (WSManDisp. h)
description: Adiciona um seletor ao objeto ResourceLocator. O seletor especifica uma instância específica de um recurso.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- método addselecter Gerenciamento Remoto do Windows
- método addselecter Gerenciamento Remoto do Windows, objeto ResourceLocator
- objeto ResourceLocator Gerenciamento Remoto do Windows, método addseletor
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc59aab6e5194716fa3b0cda98bb874d0045011c0159c5caaa3cbd53e7fbfd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121636"
---
# <a name="resourcelocatoraddselector-method"></a>Método ResourceLocator. addseletor

Adiciona um [*seletor*](windows-remote-management-glossary.md) ao objeto [**ResourceLocator**](resourcelocator.md) . O seletor especifica uma instância específica de um *recurso*. Você pode fornecer um objeto [**ResourceLocator**](resourcelocator.md) em vez de especificar um URI de recurso em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxe


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*resourceSelName* \[ no\]
</dt> <dd>

O nome do seletor. Por exemplo, ao solicitar dados WMI, esse parâmetro é a propriedade de chave para uma classe WMI.

</dd> <dt>

*selValue* \[ no\]
</dt> <dd>

O valor do seletor. Por exemplo, para dados WMI, esse parâmetro contém um valor para uma propriedade de chave que identifica uma instância específica.

</dd> </dl>

## <a name="remarks"></a>Comentários

**IWSManResourceLocator:: Addseletor** é o método C++ correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





