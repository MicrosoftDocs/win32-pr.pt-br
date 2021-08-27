---
description: Retorno de chamada para gravar uma textura como um arquivo DDS.
MS-HAID: vspixengine.ITextureCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ITextureCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2558C90A-7235-4A36-859C-0E74BD0B712A
api_name:
- ITextureCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e0d058a9851c4c9c3df3f5757b4ae3f6eb4356e
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786082"
---
# <a name="span-idvspixengineitexturecallbackspanitexturecallback-interface"></a><span id="vspixengine.itexturecallback"></span>Interface ITextureCallback

Retorno de chamada para gravar uma textura como um arquivo DDS.

## <a name="members"></a>Membros

A interface **ITextureCallback** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITextureCallback** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

A interface **ITextureCallback** tem esses métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descrição</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>Resultcallback</strong></a></td><td ><p>Um retorno de chamada que notifica o host de que o . O arquivo DDS (DirectDraw Surface) que contém os resultados da solicitação associada está pronto.</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 
