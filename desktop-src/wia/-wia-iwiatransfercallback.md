---
description: A interface IWiaTransferCallback recebe retornos de chamada durante uma transferência de dados.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interface IWiaTransferCallback (Wia.h)
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
ms.openlocfilehash: 20c577530785de3e05d00d4674556fbcd03cb69832b164e12dc703108d23c58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549636"
---
# <a name="iwiatransfercallback-interface"></a>Interface IWiaTransferCallback

A interface **IWiaTransferCallback** recebe retornos de chamada durante uma transferência de dados.

## <a name="members"></a>Membros

A interface **IWiaTransferCallback** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaTransferCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaTransferCallback** tem esses métodos.



| Método                                                                 | Descrição                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md)       | Obtém um novo fluxo para o item especificado. <br/>                    |
| [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) | Fornece progresso e outras notificações durante uma transferência. <br/> |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores de filtro de processamento de imagem devem implementar essa interface e a interface [**IWiaImageFilter.**](-wia-iwiaimagefilter.md)

A interface **IWiaTransferCallback,** como todas Component Object Model (COM), herda os métodos de interface [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Métodos IUnknown                                        | Descrição                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retorna ponteiros para interfaces com suporte. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa a contagem de referência.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Contagem de referências de decrementos.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
