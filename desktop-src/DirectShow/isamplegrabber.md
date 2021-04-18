---
description: A interface ISampleGrabber é exposta pelo filtro de apoio de exemplo. Ele permite que um aplicativo recupere exemplos de mídia individuais à medida que eles se movem pelo grafo de filtro.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interface ISampleGrabber (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810216"
---
# <a name="isamplegrabber-interface"></a>Interface ISampleGrabber

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A interface **ISampleGrabber** é exposta pelo filtro de [**apoio de exemplo**](sample-grabber-filter.md) . Ele permite que um aplicativo recupere exemplos de mídia individuais à medida que eles se movem pelo grafo de filtro.

## <a name="members"></a>Membros

A interface **ISampleGrabber** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISampleGrabber** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ISampleGrabber** tem esses métodos.



| Método                                                                | Descrição                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) | Recupera o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.<br/>                                        |
| [**GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)           | Recupera uma cópia do exemplo que o filtro recebeu mais recentemente.<br/>                                                 |
| [**GetCurrentSample**](isamplegrabber-getcurrentsample.md)           | Não implementado.<br/>                                                                                                       |
| [**SetBufferSamples**](isamplegrabber-setbuffersamples.md)           | Especifica se os dados de exemplo devem ser copiados em um buffer conforme eles passam pelo filtro.<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | Especifica um método de retorno de chamada para chamar em exemplos de entrada.<br/>                                                               |
| [**SetMediaType**](isamplegrabber-setmediatype.md)                   | Especifica o tipo de mídia para a conexão no pino de entrada do exemplo de apoio.<br/>                                    |
| [**SetOneShot**](isamplegrabber-setoneshot.md)                       | Especifica se o filtro de [**apoio de exemplo**](sample-grabber-filter.md) é interrompido depois que o filtro recebe um exemplo.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando o exemplo de apoio](using-the-sample-grabber.md)
</dt> </dl>

 

 
