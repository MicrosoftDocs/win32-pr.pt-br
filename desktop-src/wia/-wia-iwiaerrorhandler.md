---
description: A interface IWiaErrorHandler fornece métodos para tratar erros que podem ocorrer quando um aplicativo solicita dados de imagem, seja para bits de versão prévia ou final.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interface IWiaErrorHandler (Wia.h)
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
ms.openlocfilehash: 6e97c5a146c23ce1ecdb2ba77cde5d37cd9091fc9d77e288042f02fc118816e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965585"
---
# <a name="iwiaerrorhandler-interface"></a>Interface IWiaErrorHandler

A interface **IWiaErrorHandler** fornece métodos para tratar erros que podem ocorrer quando um aplicativo solicita dados de imagem, seja para bits de versão prévia ou final.

## <a name="members"></a>Membros

A interface **IWiaErrorHandler** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaErrorHandler** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaErrorHandler** tem esses métodos.



| Método                                                                     | Descrição                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Retorna uma cadeia de caracteres que descreve o código de status.<br/>                                             |
| [**Reportstatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | Lida com mensagens de erro e status durante transferências de dados de imagem e as exibe para o usuário.<br/> |



 

## <a name="remarks"></a>Comentários

O objeto de retorno de chamada do aplicativo pode implementar **IWiaErrorHandler**.

Essa interface não foi projetada para lidar com erros encontrados fora das transferências de dados de imagem, por exemplo, erros ao obter ou definir propriedades do dispositivo ou retornos de chamada não retornadas em um driver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
