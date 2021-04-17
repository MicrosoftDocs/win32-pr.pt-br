---
description: O método GetSampleGrabber recupera um ponteiro para a interface ISampleGrabber, que permite que um aplicativo recupere amostras individuais de um fluxo de mídia.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'Método IMediaDet:: GetSampleGrabber (QEdit. h)'
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
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789641"
---
# <a name="imediadetgetsamplegrabber-method"></a>Método IMediaDet:: GetSampleGrabber

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetSampleGrabber` método recupera um ponteiro para a interface [**ISampleGrabber**](isamplegrabber.md) , que permite que um aplicativo recupere amostras individuais de um fluxo de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppVal* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**ISampleGrabber**](isamplegrabber.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Chame [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) antes de chamar este método. A interface [**ISampleGrabber**](isamplegrabber.md) permite que você recupere amostras de mídia individuais do fluxo. Se você apenas precisar de um bitmap de um quadro de vídeo, chame o método [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) . A interface **ISampleGrabber** é mais flexível, mas requer mais trabalho pelo aplicativo.

Se esse método tiver sucesso, a interface [**ISampleGrabber**](isamplegrabber.md) que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




