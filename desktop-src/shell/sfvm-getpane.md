---
description: SFVM \_ GetPane pode ser alterado ou indisponível.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Mensagem de SFVM_GETPANE (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922067"
---
# <a name="sfvm_getpane-message"></a>Mensagem do SFVM \_ GETpane

\[**SFVM \_ GetPane** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Permite que o objeto de retorno de chamada forneça o painel barra de status para exibir as informações da zona da Internet. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*painel* \[ no\]
</dt> <dd>

ID do painel solicitado. Normalmente, essa é \_ a zona do painel, mas pode ser qualquer um dos valores a seguir.

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span id="PANE_NONE"></span><span id="pane_none"></span>**PAINEL \_ nenhum**


</dt> <dd>

Nenhum painel.

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>**zona do painel \_**


</dt> <dd>

O painel zona da Internet.

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PAINEL \_ offline**


</dt> <dd>

O painel offline.

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>**impressora do painel \_**


</dt> <dd>

O painel de indicação de impressão.

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>**PAINEL \_ SSL**


</dt> <dd>

O painel SSL.

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**navegação do painel \_**


</dt> <dd>

O painel de navegação.

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**progresso do painel \_**


</dt> <dd>

O painel de barra de progresso.

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**privacidade do painel \_**


</dt> <dd>

O painel de indicadores de privacidade.

</dd> </dl> </dd> <dt>

*painel* \[ fora\]
</dt> <dd>

Ponteiro para um **DWORD** que contém o número do painel.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| Fim do suporte do cliente<br/>    | Windows XP com SP2<br/>                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
