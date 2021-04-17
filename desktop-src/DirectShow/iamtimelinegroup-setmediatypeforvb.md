---
description: O método SetMediaTypeForVB especifica o tipo de mídia de grupo para clientes de automação.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'Método IAMTimelineGroup:: SetMediaTypeForVB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760883"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a>Método IAMTimelineGroup:: SetMediaTypeForVB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetMediaTypeForVB` método especifica o tipo de mídia de grupo para clientes de automação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Valor* \[ no\]
</dt> <dd>

Valor que especifica o tipo de mídia. Defina o valor como 0 para vídeo ou 1 para áudio.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método destina-se a clientes de automação. Para aplicativos C++, use o método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) .

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




