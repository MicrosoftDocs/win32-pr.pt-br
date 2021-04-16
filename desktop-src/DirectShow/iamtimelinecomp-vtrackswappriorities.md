---
description: O método VTrackSwapPriorities alterna os níveis de prioridade de duas faixas.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'Método IAMTimelineComp:: VTrackSwapPriorities (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758845"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a>Método IAMTimelineComp:: VTrackSwapPriorities

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `VTrackSwapPriorities` método alterna os níveis de prioridade de duas faixas.

Considerando dois níveis de prioridade, esse método alterna as faixas virtuais nessas prioridades. Quando o método retorna, a faixa que estava no primeiro nível de prioridade é agora no segundo nível de prioridade, e vice-versa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VirtualTrackA* 
</dt> <dd>

Primeiro nível de prioridade no qual trocar faixas virtuais.

</dd> <dt>

*VirtualTrackB* 
</dt> <dd>

Segundo nível de prioridade no qual trocar faixas virtuais.

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

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




