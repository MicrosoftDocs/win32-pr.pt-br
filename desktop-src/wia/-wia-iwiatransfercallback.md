---
description: A interface IWiaTransferCallback recebe retornos de chamada durante uma transferência de dados.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interface IWiaTransferCallback (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090501"
---
# <a name="iwiatransfercallback-interface"></a>Interface IWiaTransferCallback

A interface **IWiaTransferCallback** recebe retornos de chamada durante uma transferência de dados.

## <a name="members"></a>Membros

A interface **IWiaTransferCallback** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaTransferCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaTransferCallback** tem esses métodos.



| Método                                                                 | Descrição                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md)       | Obtém um novo fluxo para o item especificado. <br/>                    |
| [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) | Fornece o progresso e outras notificações durante uma transferência. <br/> |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores de filtro de processamento de imagens devem implementar essa interface e a interface [**IWiaImageFilter**](-wia-iwiaimagefilter.md) .

A interface **IWiaTransferCallback** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descrição                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retorna ponteiros para interfaces com suporte. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa a contagem de referência.               |
| [IUnknown:: versão](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Decrementa a contagem de referência.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
