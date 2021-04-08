---
description: A interface IWiaUIExtension2 fornece métodos que substituem a interface do usuário padrão fornecida pelo sistema por uma interface do usuário personalizada e que fornecem um ícone de dispositivo personalizado.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interface IWiaUIExtension2 (Wiadevd. h)
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
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920950"
---
# <a name="iwiauiextension2-interface"></a>Interface IWiaUIExtension2

A interface IWiaUIExtension2 fornece métodos que substituem a interface do usuário padrão fornecida pelo sistema por uma interface do usuário personalizada e que fornecem um ícone de dispositivo personalizado. Os fornecedores de dispositivos podem implementar essa interface para fornecer interfaces de usuário personalizadas para seus dispositivos.

## <a name="members"></a>Membros

A interface **IWiaUIExtension2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaUIExtension2** também tem estes tipos de membros:

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
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retorna ponteiros para interfaces com suporte. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa a contagem de referência.               |
| [IUnknown:: versão](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Decrementa a contagem de referência.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 
