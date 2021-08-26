---
description: Solicitação de uma textura de lado-a-escrita como um arquivo DDS.
MS-HAID: vspixengine.ITileRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ITileRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DBA493E7-EBB6-490D-BDC6-946265A474D6
api_name:
- ITileRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b0a5f31e68f53f316ea77f77f2ff778eb817e11c
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786162"
---
# <a name="span-idvspixengineitilerequestspanitilerequest-interface"></a><span id="vspixengine.itilerequest"></span>Interface ITileRequest

Solicitação de uma textura de lado-a-escrita como um arquivo DDS.

## <a name="members"></a>Membros

A interface **ITileRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITileRequest** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>Métodos

A interface **ITileRequest** tem esses métodos.

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >Método</th><th >Descrição</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/itilerequest-requestbuffertileasync-eventid-dword-bstr-uint-ibufferobjectdatacallback-ptr-dword-dword"><strong>RequestBufferTileAsync</strong></a></td><td ><p>Solicitações para obter o conteúdo bruto de um bloco.</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/itilerequest-requesttexturetileasync-eventid-dword-uint-uint-uint-uint-bstr-itexturecallback-ptr-dword-dword"><strong>RequestTextureTileAsync</strong></a></td><td ><p>Solicitações para obter o conteúdo de uma textura com um lado do ladrilho como um. Arquivo DDS (superfície do DirectDraw).</p></td></tr></tbody></table>

 

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Cabeçalho</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 
