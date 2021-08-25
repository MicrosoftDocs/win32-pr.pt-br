---
description: O método ZeroBetween remove tudo da faixa entre os horários especificados. Esse método divide todos os objetos que abrangem o intervalo de tempo especificado e remove as partes que estão dentro do intervalo.
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: 'Método IAMTimelineTrack:: ZeroBetween (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b5ec57833ed34a432988c42351a333362168112174cccd7a989e0c2e1bddd694
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982896"
---
# <a name="iamtimelinetrackzerobetween-method"></a>Método IAMTimelineTrack:: ZeroBetween

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ZeroBetween` método remove tudo da faixa entre os horários especificados. Esse método divide todos os objetos que abrangem o intervalo de tempo especificado e remove as partes que estão dentro do intervalo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtStart* 
</dt> <dd>

Início do intervalo a ser limpo, em unidades de 100 a nanossegundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Fim do intervalo a ser limpo, em unidades de 100 a nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                             | Descrição                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O intervalo de tempo cai além de tudo na faixa.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                             |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




