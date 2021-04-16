---
description: O método SetBufferSamples especifica se os dados de exemplo devem ser copiados em um buffer conforme eles passam pelo filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'Método ISampleGrabber:: SetBufferSamples (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759283"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>Método ISampleGrabber:: SetBufferSamples

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método **SetBufferSamples** especifica se os dados de exemplo devem ser copiados em um buffer conforme eles passam pelo filtro.

## <a name="syntax"></a>Sintaxe


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*BufferThem* 
</dt> <dd>

Valor booliano que especifica se os dados de exemplo devem ser armazenados em buffer. Se **for true**, o filtro copiará dados de exemplo em um buffer interno.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para obter o buffer copiado, chame [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).

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
</dt> <dt>

[**Interface ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




