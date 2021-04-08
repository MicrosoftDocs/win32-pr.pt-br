---
description: A interface IWiaDevMgr2 é usada para criar e gerenciar dispositivos de aquisição de imagem e para se registrar para receber eventos de dispositivo.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Interface IWiaDevMgr2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828453"
---
# <a name="iwiadevmgr2-interface"></a>Interface IWiaDevMgr2

A interface **IWiaDevMgr2** é usada para criar e gerenciar dispositivos de aquisição de imagem e para se registrar para receber eventos de dispositivo.

## <a name="members"></a>Membros

A interface **IWiaDevMgr2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaDevMgr2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaDevMgr2** tem esses métodos.



| Método                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDevice**](-wia-iwiadevmgr2-createdevice.md)                                     | Cria uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para um dispositivo WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                 |
| [**EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | Cria um enumerador de informações de propriedade para cada dispositivo WIA 2,0 disponível. <br/>                                                                                                                                                                                                                                                                                                                 |
| [**GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)                                       | O método [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) exibe uma ou mais caixas de diálogo que permitem que um usuário adquira uma imagem de um dispositivo WIA 2,0 e grave a imagem em um arquivo especificado. Esse método estende a funcionalidade de [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular a aquisição de imagem em uma única chamada à API. <br/> |
| [**RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | O método [**IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) registra um aplicativo para receber eventos, mesmo que o aplicativo não esteja em execução.<br/>                                                                                                                                                                                                      |
| [**RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) | Registra um aplicativo em execução para notificação de eventos WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | O método [**IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) registra um aplicativo para receber eventos de dispositivo. Ele é fornecido principalmente para compatibilidade com versões anteriores com aplicativos que não foram escritos para o WIA 2,0.<br/>                                                                                                                         |
| [**SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md)                               | Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem. <br/>                                                                                                                                                                                                                                                                                                   |
| [**SelectDeviceDlgID**](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem. <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

A interface **IWiaDevMgr2** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descrição                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retorna ponteiros para interfaces com suporte. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa a contagem de referência.               |
| [IUnknown:: versão](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Decrementa a contagem de referência.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
