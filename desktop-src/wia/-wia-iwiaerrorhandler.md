---
description: A interface IWiaErrorHandler fornece métodos para lidar com erros que podem ocorrer quando um aplicativo solicita dados de imagem, seja para os bits de visualização ou final.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interface IWiaErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090802"
---
# <a name="iwiaerrorhandler-interface"></a>Interface IWiaErrorHandler

A interface **IWiaErrorHandler** fornece métodos para lidar com erros que podem ocorrer quando um aplicativo solicita dados de imagem, seja para os bits de visualização ou final.

## <a name="members"></a>Membros

A interface **IWiaErrorHandler** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaErrorHandler** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaErrorHandler** tem esses métodos.



| Método                                                                     | Descrição                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Retorna uma cadeia de caracteres que descreve o código de status.<br/>                                             |
| [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | Manipula mensagens de status e de erro durante transferências de dados de imagem e as exibe para o usuário.<br/> |



 

## <a name="remarks"></a>Comentários

O objeto de retorno de chamada do aplicativo pode implementar **IWiaErrorHandler**.

Esta interface não foi projetada para lidar com erros encontrados fora das transferências de dados de imagem, por exemplo, erros ao obter ou definir propriedades de dispositivo ou retornos de chamada não retornados em um driver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
