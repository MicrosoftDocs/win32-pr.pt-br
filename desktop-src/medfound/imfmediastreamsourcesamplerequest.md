---
description: Representa uma solicitação de um exemplo de um MediaStreamSource.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Interface IMFMediaStreamSourceSampleRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297951"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a>Interface IMFMediaStreamSourceSampleRequest

Representa uma solicitação de um exemplo de um MediaStreamSource.

## <a name="members"></a>Membros

A interface **IMFMediaStreamSourceSampleRequest** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMFMediaStreamSourceSampleRequest** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMFMediaStreamSourceSampleRequest** tem esses métodos.



| Método                                                           | Descrição                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**Setsample**](imfmediastreamsourcesamplerequest-setsample.md) | Define o exemplo para a origem do fluxo de mídia.<br/> |



 

## <a name="remarks"></a>Comentários

**MFMediaStreamSourceSampleRequest** é implementado pela classe de tempo de execução [**Windows. Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                       |
| INSERI<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces Media Foundation](media-foundation-interfaces.md)
</dt> </dl>

 

 
