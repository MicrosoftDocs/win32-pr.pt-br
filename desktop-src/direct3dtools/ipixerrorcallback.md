---
description: Retorno de chamada do mecanismo para tratar erros.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixErrorCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 89900bf3ea6816bbb0a6fa307f4d17c08a4c3e5a
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786112"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span id="vspixengine.ipixerrorcallback"></span>Interface IPixErrorCallback

Retorno de chamada do mecanismo para tratar erros.

## <a name="members"></a>Membros

A interface **IPixErrorCallback** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPixErrorCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

A interface **IPixErrorCallback** tem esses métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descrição</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></td><td ><p>Um retorno de chamada que notifica o host de erros retornados pela solicitação associada.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></td><td ><p>Um retorno de chamada que notifica o host de mensagens retornadas pela solicitação associada.</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></td><td ><p>Um retorno de chamada que notifica o host de avisos retornados pela solicitação associada.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
