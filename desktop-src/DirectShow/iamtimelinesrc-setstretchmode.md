---
description: O método setstretchmode define o modo de ampliação. O modo de ampliação determina como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'Método IAMTimelineSrc:: setstretchmode (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761759"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a>Método IAMTimelineSrc:: setstretchmode

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetStretchMode` método define o modo Stretch. O modo de ampliação determina como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nStretchMode* 
</dt> <dd>

Sinalizador que indica o modo de Stretch atual. Para obter uma lista de valores possíveis, consulte [**redimensionar sinalizadores**](resize-flags.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




