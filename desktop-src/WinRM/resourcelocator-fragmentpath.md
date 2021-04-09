---
title: Propriedade ResourceLocator. FragmentPath (WSManDisp. h)
description: Obtém ou define o caminho para um fragmento de recurso ou propriedade quando ResourceLocator é usado em operações de objeto de sessão, como Session. Get, Session. Put ou Session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows da propriedade FragmentPath
- Propriedade FragmentPath Gerenciamento Remoto do Windows, objeto ResourceLocator
- Objeto ResourceLocator Gerenciamento Remoto do Windows, Propriedade FragmentPath
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
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009407"
---
# <a name="resourcelocatorfragmentpath-property"></a>Propriedade ResourceLocator. FragmentPath

Obtém ou define o caminho para um [](windows-remote-management-glossary.md) [*fragmento*](windows-remote-management-glossary.md) de recurso ou propriedade quando [**ResourceLocator**](resourcelocator.md) é usado em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a>Valor da propriedade

Cadeia de caracteres que identifica o fragmento ou a propriedade do recurso. Por exemplo, se o recurso for uma unidade de disco e a propriedade solicitada for fabricante, a cadeia de caracteres poderá conter `Diskdrive/Manufacturer` . O texto do fragmento diferencia maiúsculas de minúsculas. Nesse caso, você não pode usar `diskdrive/manufacturer` .

## <a name="remarks"></a>Comentários

**IWSManResourceLocator:: FragmentPath** é a propriedade C++ correspondente.

Você pode especificar um elemento de uma propriedade de matriz fornecendo o índice de matriz, conforme mostrado no exemplo a seguir. Lembre-se de que a indexação de matriz começa com 1 em vez de 0.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



Para obter a matriz inteira, especifique o nome da propriedade de matriz, conforme mostrado no exemplo a seguir.


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



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

 

 





