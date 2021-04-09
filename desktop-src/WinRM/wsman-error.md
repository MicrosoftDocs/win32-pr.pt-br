---
title: Propriedade WSMan. Error (WSManDisp. h)
description: Obtém informações de erro adicionais, em um fluxo XML, para a chamada anterior para um método WSMan se Gerenciamento Remoto do Windows serviço não pôde criar um objeto de sessão, um objeto ConnectionOptions ou um objeto ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de propriedade de erro
- Propriedade de erro Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, Propriedade Error
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
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085597"
---
# <a name="wsmanerror-property"></a>Propriedade WSMan. Error

Obtém informações de erro adicionais, em um fluxo XML, para a chamada anterior para um método [**WSMan**](wsman.md) se gerenciamento remoto do Windows serviço não pôde criar um objeto de [**sessão**](session.md) , um objeto [**ConnectionOptions**](connectionoptions.md) ou um objeto [**ResourceLocator**](resourcelocator.md) .

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
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





