---
description: O método IsNormalRate indica se o clipe será reproduzido na taxa de reprodução normal; ou seja, a taxa de reprodução do arquivo original.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'Método IAMTimelineSrc:: IsNormalRate (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780057"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>Método IAMTimelineSrc:: IsNormalRate

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `IsNormalRate` método indica se o clipe será reproduzido na taxa de reprodução normal; ou seja, a taxa de reprodução do arquivo original.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recebe um valor booliano que indica como o clipe será renderizado. Se o valor for **true**, o clipe será reproduzido na taxa normal. Caso contrário, ele será executado mais rápido ou mais devagar do que o normal.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

A taxa de reprodução de um clipe é determinada por seus horários de início e parada de mídia, em relação às horas da linha do tempo:


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



Se essa taxa for igual a 1, o clipe será reproduzido na velocidade criada. Caso contrário, ele será executado mais rápido ou mais devagar. Para obter mais informações, consulte [tempo em serviços de edição do DirectShow](time-in-directshow-editing-services.md).

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

 

 




