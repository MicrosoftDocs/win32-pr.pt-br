---
description: A interface IWiaTransfer fornece transferência de dados baseada em fluxo.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interface IWiaTransfer (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164528"
---
# <a name="iwiatransfer-interface"></a>Interface IWiaTransfer

A interface **IWiaTransfer** fornece transferência de dados baseada em fluxo.

## <a name="members"></a>Membros

A interface **IWiaTransfer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaTransfer** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaTransfer** tem esses métodos.



| Método                                                                 | Descrição                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Cancelar**](-wia-iwiatransfer-cancel.md)                             | Cancela a operação de transferência atual. <br/>                                         |
| [**Baixar**](-wia-iwiatransfer-download.md)                         | Inicia um download de dados para o chamador. <br/>                                        |
| [**\_Informações do formato EnumWIA \_**](-wia-iwiatransfer-enumwia-format-info.md) | Cria um enumerador para os formatos de transferência aos quais o dispositivo WIA 2,0 dá suporte.<br/> |
| [**Carregar**](-wia-iwiatransfer-upload.md)                             | Inicia um carregamento de dados de um único item do chamador. <br/>                       |



 

## <a name="remarks"></a>Comentários

A interface **IWiaTransfer** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



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



 

 
