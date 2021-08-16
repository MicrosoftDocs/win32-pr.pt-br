---
description: A interface IWiaUIExtension2 fornece métodos que substituem a interface do usuário padrão fornecida pelo sistema por uma interface do usuário personalizada e que fornecem um ícone de dispositivo personalizado.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interface IWiaUIExtension2 (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 2111c25a83a9b826f4cab7dba8f689e01a9868ac416b8fb3026f1b1fb49a90ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208139"
---
# <a name="iwiauiextension2-interface"></a>Interface IWiaUIExtension2

A interface IWiaUIExtension2 fornece métodos que substituem a interface do usuário padrão fornecida pelo sistema por uma interface do usuário personalizada e que fornecem um ícone de dispositivo personalizado. Os fornecedores de dispositivos podem implementar essa interface para fornecer interfaces de usuário personalizadas para seus dispositivos.

## <a name="members"></a>Membros

A interface **IWiaUIExtension2** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IWiaUIExtension2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaUIExtension2** tem esses métodos.



| Método                                                       | Descrição                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension2-devicedialog.md)   | Fornece uma interface do usuário personalizada que substitui a interface do usuário do sistema padrão.<br/> |
| [**GetDeviceIcon**](-wia-iwiauiextension2-getdeviceicon.md) | Obtém um ícone de dispositivo personalizado.<br/>                                                        |



 

## <a name="remarks"></a>Comentários



| Métodos IUnknown                                        | Descrição                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retorna ponteiros para interfaces com suporte. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa a contagem de referência.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Contagem de referências de decrementos.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl> |



 

 
