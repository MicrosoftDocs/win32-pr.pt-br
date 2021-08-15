---
title: Propriedade WSMan.Error (WSManDisp.h)
description: Obtém informações de erro adicionais, em um fluxo XML, para a chamada anterior a um método WSMan se o serviço de Gerenciamento Remoto do Windows não pôde criar um objeto Session, um objeto ConnectionOptions ou um objeto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Propriedade error Windows Remote Management
- Propriedade error Windows Remote Management , objeto WSMan
- Objeto WSMan Windows Gerenciamento Remoto, propriedade Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d72c99150d3c6ac95e91e6a9674ab6364e8ea46fabf3d58d50556e129933cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742191"
---
# <a name="wsmanerror-property"></a>Propriedade WSMan.Error

Obtém informações de erro adicionais, em um fluxo XML, para a chamada anterior para um método [**WSMan**](wsman.md) se o serviço de Gerenciamento Remoto do Windows não pôde criar um objeto [**Session,**](session.md) um objeto [**ConnectionOptions**](connectionoptions.md) ou um [**objeto ResourceLocator.**](resourcelocator.md)

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a>Valor da propriedade

A representação XML das informações de erro.

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

[**Wsman**](wsman.md)
</dt> </dl>

 

 





