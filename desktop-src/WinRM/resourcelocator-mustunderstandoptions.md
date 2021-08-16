---
title: Propriedade ResourceLocator.MustUnderstandOptions (WSManDisp.h)
description: Obtém ou define o valor MustUnderstandOptions para o objeto ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Propriedade MustUnderstandOptions Windows Gerenciamento Remoto
- Propriedade MustUnderstandOptions Windows gerenciamento remoto, objeto ResourceLocator
- Objeto ResourceLocator Windows Gerenciamento Remoto , propriedade MustUnderstandOptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a49c3af0372553c221dae902a5fdca0e026bb874f612b8e21f41e6a6870f7ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323734"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>Propriedade ResourceLocator.MustUnderstandOptions

Obtém ou define o **valor MustUnderstandOptions** para o [**objeto ResourceLocator.**](resourcelocator.md) Você pode fornecer um [**objeto ResourceLocator**](resourcelocator.md) em vez [](session.md) de especificar um URI de recurso em operações de objeto session, como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)ou [**Session.Enumerate**](session-enumerate.md).

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Valor da propriedade

Indica, quando **True**, que o [](ws-management-protocol.md) serviço que implementa o protocolo WS-Management deverá retornar um erro se ele não for capaz de processar a opção.

## <a name="remarks"></a>Comentários

**IWSManResourceLocator::MustUnderstandOptions** é a propriedade C++ correspondente.

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

 

 





