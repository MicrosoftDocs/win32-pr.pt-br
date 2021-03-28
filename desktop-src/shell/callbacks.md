---
description: Esta seção descreve as funções de retorno de chamada do shell do Windows.
title: Funções de retorno de chamada do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370616"
---
# <a name="shell-callback-functions"></a>Funções de retorno de chamada do Shell

Esta seção descreve as funções de retorno de chamada do shell do Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                     | Descrição                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Especifica uma função de retorno de chamada definida pelo aplicativo usada para enviar mensagens e processar mensagens de, uma caixa de diálogo de **procura** exibida em resposta a uma chamada para [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).<br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos para se comunicar com uma extensão do Gerenciador de arquivos.<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | Usado para determinar se um item está presente em uma lista de MRU (usado mais recentemente).<br/>                                                                                                                                   |
| [**\_rotina de alteração de PAPPSTATE \_**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Especifica uma função de retorno de chamada definida pelo aplicativo que notifica o aplicativo quando o aplicativo está entrando ou saindo de um estado suspenso.<br/>                                                                                            |
| [**SUBCLASSPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Define o protótipo para a função de retorno de chamada usada por [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) e [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).<br/>                                                   |
| [**\_proc de DESexclusão de FM \_**](undeletefile.md)<br/>                     | Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos quando o usuário escolhe o comando **restaurar** no menu **arquivo** .<br/>                                                                   |



 

 

 
