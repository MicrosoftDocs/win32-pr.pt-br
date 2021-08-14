---
description: esta seção descreve as Windows funções de retorno de chamada do Shell.
title: Funções de retorno de chamada do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d3fd334dd49d2b9cec3322630866fde4a99ccad0b5f253dd7253e551264737a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460839"
---
# <a name="shell-callback-functions"></a>Funções de retorno de chamada do Shell

esta seção descreve as Windows funções de retorno de chamada do Shell.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                     | Descrição                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Especifica uma função de retorno de chamada definida pelo aplicativo usada para enviar mensagens e processar mensagens de, uma caixa de diálogo de **procura** exibida em resposta a uma chamada para [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).<br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos para se comunicar com uma extensão do Gerenciador de arquivos.<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | Usado para determinar se um item está presente em uma lista de MRU (usado mais recentemente).<br/>                                                                                                                                   |
| [**\_rotina de alteração de PAPPSTATE \_**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Especifica uma função de retorno de chamada definida pelo aplicativo que notifica o aplicativo quando o aplicativo está entrando ou saindo de um estado suspenso.<br/>                                                                                            |
| [**SUBCLASSPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Define o protótipo para a função de retorno de chamada usada por [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) e [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).<br/>                                                   |
| [**\_proc de DESexclusão de FM \_**](undeletefile.md)<br/>                     | Especifica uma função de chamada de retorno definida pelo aplicativo chamada pelo Gerenciador de arquivos quando o usuário escolhe o comando **restaurar** no menu **arquivo** .<br/>                                                                   |



 

 

 
