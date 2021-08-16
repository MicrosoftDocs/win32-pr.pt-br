---
description: O método GetSampleGrabber recupera um ponteiro para a interface ISampleGrabber, que permite que um aplicativo recupere amostras individuais de um fluxo de mídia.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: Método IMediaDet::GetSampleGrabber (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f2c3c580a44b9cff35d7ee801cfc611b5cf8a8df828f54c28b022e5c1a1b862a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819037"
---
# <a name="imediadetgetsamplegrabber-method"></a>Método IMediaDet::GetSampleGrabber

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetSampleGrabber` método recupera um ponteiro para a interface [**ISampleGrabber,**](isamplegrabber.md) que permite que um aplicativo recupere amostras individuais de um fluxo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppVal* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**ISampleGrabber.**](isamplegrabber.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Chame [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) antes de chamar esse método. A interface [**ISampleGrabber**](isamplegrabber.md) permite que você recupere amostras de mídia individuais do fluxo. Se você precisar apenas de um bitmap de um quadro de vídeo, chame o [**método IMediaDet::GetBitmapBits.**](imediadet-getbitmapbits.md) A interface **ISampleGrabber** é mais flexível, mas requer mais trabalho pelo aplicativo.

Se esse método for bem-sucedido, a interface [**ISampleGrabber**](isamplegrabber.md) retornada terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**IMediaDet Interface**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




