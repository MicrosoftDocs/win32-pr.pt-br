---
title: Propriedade ResourceLocator.FragmentPath (WSManDisp.h)
description: Obtém ou define o caminho para um fragmento de recurso ou propriedade quando ResourceLocator é usado em operações de objeto session, como Session.Get, Session.Put ou Session.Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Propriedade FragmentPath Windows Gerenciamento Remoto
- Propriedade FragmentPath Windows gerenciamento remoto, objeto ResourceLocator
- Objeto ResourceLocator Windows Gerenciamento Remoto, propriedade FragmentPath
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f756d669ba79ce034a9562d6cae5d58653bc60e042344306fb18aa37edfdc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121626"
---
# <a name="resourcelocatorfragmentpath-property"></a>Propriedade ResourceLocator.FragmentPath

Obtém ou define [](windows-remote-management-glossary.md) [](windows-remote-management-glossary.md) o caminho para um fragmento de [](session.md) recurso ou propriedade quando [**ResourceLocator**](resourcelocator.md) é usado em operações de objeto session, [**como Session.Get**](session-get.md), [**Session.Put**](session-put.md)ou [**Session.Enumerate**](session-enumerate.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Valor da propriedade

Cadeia de caracteres que identifica o fragmento ou a propriedade do recurso. Por exemplo, se o recurso for uma unidade de disco e a propriedade solicitada for Fabricante, a cadeia de caracteres poderá conter `Diskdrive/Manufacturer` . O texto do fragmento faz a ressição de minúsculas. Nesse caso, você não pode usar `diskdrive/manufacturer` .

## <a name="remarks"></a>Comentários

**IWSManResourceLocator::FragmentPath** é a propriedade C++ correspondente.

Você pode especificar um elemento de uma propriedade de matriz fornecendo o índice de matriz, conforme mostrado no exemplo a seguir. Esteja ciente de que a indexação de matriz começa com 1 em vez de 0.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Para obter toda a matriz, especifique o nome da propriedade da matriz, conforme mostrado no exemplo a seguir.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



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

 

 





