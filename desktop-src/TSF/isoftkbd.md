---
title: Interface ISoftKbd (Softkbdc. h)
description: A interface ISoftKbd é usada por aplicativos e serviços de texto para implementar um teclado virtual.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Estrutura de serviços de texto da interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, descrita
topic_type:
- apiref
api_name:
- ISoftKbd
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e046964616fc564aa2e0c3d0098ee2186cdaf8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761367"
---
# <a name="isoftkbd-interface"></a>Interface ISoftKbd

A interface **ISoftKbd** é usada por aplicativos e serviços de texto para implementar um teclado virtual.

## <a name="members"></a>Membros

A interface **ISoftKbd** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ISoftKbd** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISoftKbd** tem esses métodos.



| Método                                                                                        | Descrição                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**AdviseSoftKeyboardEventSink**](isoftkbd-advisesoftkeyboardeventsink.md)                   | Instala um coletor de eventos de teclado flexível para lidar com notificações OnKeySelection do teclado soft.<br/> |
| [**CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md) | Cria um layout de teclado flexível a partir do recurso especificado.<br/>                                        |
| [**CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | Cria um layout de teclado flexível a partir do arquivo XML especificado.<br/>                                        |
| [**CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)                         | Cria uma janela de teclado flexível.<br/>                                                                    |
| [**DestroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)                       | Destrói uma janela de teclado flexível.<br/>                                                                   |
| [**EnumSoftKeyboard**](isoftkbd-enumsoftkeyboard.md)                                         | Enumera os teclados suaves possíveis que dão suporte ao idioma especificado.<br/>                        |
| [**GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)                               | Recupera a cor do teclado flexível correspondente ao tipo de cor fornecido.<br/>                        |
| [**GetSoftKeyboardPosSize**](isoftkbd-getsoftkeyboardpossize.md)                             | Recupera a posição inicial e o tamanho de um teclado suave.<br/>                                       |
| [**GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)                           | Recupera a fonte de texto usada por um teclado virtual.<br/>                                                   |
| [**GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)                           | Recupera o modo de tipo para um teclado virtual.<br/>                                                       |
| [**Inicializar**](isoftkbd-initialize.md)                                                     | Inicializa todos os campos necessários para um teclado virtual e gera layouts de teclado flexível padrão.<br/> |
| [**SelectSoftKeyboard**](isoftkbd-selectsoftkeyboard.md)                                     | Seleciona o teclado virtual especificado.<br/>                                                               |
| [**SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)                                 | Define o texto do rótulo do layout de um teclado virtual.<br/>                                           |
| [**SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)           | Define uma combinação de rótulo e texto usado para descrever um teclado suave.<br/>                             |
| [**SetSoftKeyboardColors**](isoftkbd-setsoftkeyboardcolors.md)                               | Define a cor do teclado flexível correspondente ao tipo de cor fornecido.<br/>                             |
| [**SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)                             | Define a posição inicial e o tamanho de um teclado suave.<br/>                                            |
| [**SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)                           | Define a fonte de texto usada por um teclado virtual.<br/>                                                        |
| [**SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)                           | Define o modo de tipo para um teclado virtual.<br/>                                                            |
| [**ShowKeysForKeyScanMode**](isoftkbd-showkeysforkeyscanmode.md)                             | Exibe as chaves usadas para o modo de verificação de chave para um teclado virtual.<br/>                                  |
| [**ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)                                         | Exibe um teclado virtual.<br/>                                                                          |
| [**UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)               | Remove um coletor de eventos de teclado flexível.<br/>                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



 

