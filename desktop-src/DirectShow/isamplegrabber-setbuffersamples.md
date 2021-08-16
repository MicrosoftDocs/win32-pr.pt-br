---
description: O método SetBufferSamples especifica se os dados de exemplo serão copiados em um buffer conforme ele passa pelo filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: Método ISampleGrabber::SetBufferSamples (Qedit.h)
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
ms.openlocfilehash: c768a21d4e08e6900f3a46f3e398f5040aaf6b6b0bc45c9187ac07821500a372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817991"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>Método ISampleGrabber::SetBufferSamples

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O **método SetBufferSamples** especifica se os dados de exemplo serão copiados em um buffer conforme ele passa pelo filtro.

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

Valor booliana que especifica se os dados de exemplo devem ser armazenados em buffer. Se **TRUE**, o filtro copia dados de exemplo em um buffer interno.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para obter o buffer copiado, chame [**ISampleGrabber::GetCurrentBuffer.**](isamplegrabber-getcurrentbuffer.md)

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando o exemplo de grabber](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber Interface**](isamplegrabber.md)
</dt> </dl>

 

 




