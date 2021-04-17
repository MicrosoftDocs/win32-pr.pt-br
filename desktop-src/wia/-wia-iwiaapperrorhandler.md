---
description: A interface IWiaAppErrorHandler permite que os aplicativos exibam janelas de erro (durante transferências de dados) da qual o usuário pode escolher se deseja continuar, cancelar ou anular a transferência.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interface IWiaAppErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105795469"
---
# <a name="iwiaapperrorhandler-interface"></a>Interface IWiaAppErrorHandler

A interface **IWiaAppErrorHandler** permite que os aplicativos exibam janelas de erro (durante transferências de dados) da qual o usuário pode escolher se deseja continuar, cancelar ou anular a transferência.

## <a name="members"></a>Membros

A interface **IWiaAppErrorHandler** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaAppErrorHandler** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaAppErrorHandler** tem esses métodos.



| Método                                                        | Descrição                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | Obtém um identificador para a caixa de diálogo que exibe mensagens de erro e fornece um ou mais botões para continuar, cancelar ou anular o aplicativo.<br/> |
| [**ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) | Lida com o status do dispositivo e mensagens de erro durante transferências de dados de imagem e exibe as mensagens para o usuário.<br/>                                  |



 

## <a name="remarks"></a>Comentários

O objeto de tratamento de erros, ou retorno de chamada, que implementa essa interface é passado para [**IWiaTransfer::D aixar**](-wia-iwiatransfer-download.md) e [**IWiaTransfer:: upload**](-wia-iwiatransfer-upload.md).

Esta interface não foi projetada para lidar com erros encontrados fora das transferências de dados de imagem, por exemplo, erros ao obter ou definir propriedades de dispositivo ou retornos de chamada não retornados em um driver.

Um manipulador de erro de driver deve implementar [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md), em vez de **IWiaAppErrorHandler**.

O objeto que implementa essa interface também deve implementar [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).

Se você quiser um manipulador de erro de driver e um manipulador de erro padrão para exibir as janelas de mensagens de erro, mas não quiser criar um manipulador de erro completo para o aplicativo, implemente essa interface e também implemente o método [**IWiaAppErrorHandler:: ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) para retornar o \_ status WIA \_ não \_ Tratado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
