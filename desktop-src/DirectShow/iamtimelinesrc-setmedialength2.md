---
description: 'O método SetMediaLength2 especifica a duração do arquivo de origem. Esse método é equivalente a IAMTimelineSrc:: SetMediaLength, mas usa um valor de REFTIME.'
ms.assetid: 1a1dcf23-2041-4791-bce7-0ecbe33df592
title: 'Método IAMTimelineSrc:: SetMediaLength2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4deb42cdd917fe7d79a420b15247b4bdf5ee52bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779534"
---
# <a name="iamtimelinesrcsetmedialength2-method"></a>Método IAMTimelineSrc:: SetMediaLength2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaLength2` método especifica a duração do arquivo de origem. Esse método é equivalente a [**IAMTimelineSrc:: SetMediaLength**](iamtimelinesrc-setmedialength.md), mas usa um valor de [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaLength2(
   REFTIME Length
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Comprimento* 
</dt> <dd>

Comprimento da mídia, em segundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

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

 

 




