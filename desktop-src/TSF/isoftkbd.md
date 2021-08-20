---
title: Interface ISoftKbd (Softkbdc.h)
description: A interface ISoftKbd é usada por aplicativos e serviços de texto para implementar um teclado suave.
ms.assetid: 804634bd-646e-459f-9fbb-cd6929b11fab
keywords:
- Interface ISoftKbd Estrutura de Serviços de Texto
- Interface ISoftKbd Estrutura de Serviços de Texto , descrita
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
ms.openlocfilehash: e9a1bc49be78262e8d78f32c87dd2bc93b6c1405ec444329f908c8f41319e3d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952384"
---
# <a name="isoftkbd-interface"></a>Interface ISoftKbd

A **interface ISoftKbd** é usada por aplicativos e serviços de texto para implementar um teclado suave.

## <a name="members"></a>Membros

A interface **ISoftKbd** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **O ISoftKbd** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISoftKbd** tem esses métodos.



| Método                                                                                        | Descrição                                                                                                   |
|:----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**AdviseSoftKeyboardEventSink**](isoftkbd-advisesoftkeyboardeventsink.md)                   | Instala um sink de evento de teclado suave para manipular notificações onKeySelection do teclado soft.<br/> |
| [**CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md) | Cria um layout de teclado suave do recurso especificado.<br/>                                        |
| [**CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)   | Cria um layout de teclado suave do arquivo XML especificado.<br/>                                        |
| [**CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)                         | Cria uma janela de teclado suave.<br/>                                                                    |
| [**DestroySoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)                       | Destrói uma janela de teclado suave.<br/>                                                                   |
| [**EnumSoftKeyboard**](isoftkbd-enumsoftkeyboard.md)                                         | Enumera os possíveis teclados suaves que suportam o idioma especificado.<br/>                        |
| [**GetSoftKeyboardColors**](isoftkbd-getsoftkeyboardcolors.md)                               | Recupera a cor do teclado suave correspondente ao tipo de cor fornecido.<br/>                        |
| [**GetSoftKeyboardPosSize**](isoftkbd-getsoftkeyboardpossize.md)                             | Recupera a posição inicial e o tamanho de um teclado suave.<br/>                                       |
| [**GetSoftKeyboardTextFont**](isoftkbd-getsoftkeyboardtextfont.md)                           | Recupera a fonte de texto usada por um teclado suave.<br/>                                                   |
| [**GetSoftKeyboardTypeMode**](isoftkbd-getsoftkeyboardtypemode.md)                           | Recupera o modo de tipo para um teclado suave.<br/>                                                       |
| [**Inicializar**](isoftkbd-initialize.md)                                                     | Inicializa todos os campos necessários para um teclado soft e gera layouts de teclado soft padrão.<br/> |
| [**SelectSoftKeyboard**](isoftkbd-selectsoftkeyboard.md)                                     | Seleciona o teclado soft especificado.<br/>                                                               |
| [**SetKeyboardLabelText**](isoftkbd-setkeyboardlabeltext.md)                                 | Define o texto do rótulo do layout para um teclado suave.<br/>                                           |
| [**SetKeyboardLabelTextCombination**](isoftkbd-setkeyboardlabeltextcombination.md)           | Define uma combinação de rótulo e texto usado para descrever um teclado suave.<br/>                             |
| [**SetSoftKeyboardColors**](isoftkbd-setsoftkeyboardcolors.md)                               | Define a cor do teclado suave correspondente ao tipo de cor fornecido.<br/>                             |
| [**SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)                             | Define a posição inicial e o tamanho de um teclado suave.<br/>                                            |
| [**SetSoftKeyboardTextFont**](isoftkbd-setsoftkeyboardtextfont.md)                           | Define a fonte de texto usada por um teclado suave.<br/>                                                        |
| [**SetSoftKeyboardTypeMode**](isoftkbd-setsoftkeyboardtypemode.md)                           | Define o modo de tipo para um teclado suave.<br/>                                                            |
| [**ShowKeysForKeyScanMode**](isoftkbd-showkeysforkeyscanmode.md)                             | Exibe as teclas usadas para o modo de verificação de tecla para um teclado suave.<br/>                                  |
| [**ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)                                         | Exibe um teclado suave.<br/>                                                                          |
| [**UnadviseSoftKeyboardEventSink**](isoftkbd-unadvisesoftkeyboardeventsink.md)               | Remove um sink de evento de teclado suave.<br/>                                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                        |
| Cabeçalho<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



 

