---
description: O método GetMediaTimes recupera os horários de início e de parada da mídia.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: 'Método IAMTimelineSrc:: GetMediaTimes (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa6e9cbb69da504a929e23722068583489063b9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760086"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a>Método IAMTimelineSrc:: GetMediaTimes

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetMediaTimes` método recupera os horários de início e de parada da mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStart* 
</dt> <dd>

Recebe a hora de início da mídia, em unidades de 100 a nanossegundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recebe a hora de parada da mídia, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os horários de mídia são relativos ao arquivo de mídia original. Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




