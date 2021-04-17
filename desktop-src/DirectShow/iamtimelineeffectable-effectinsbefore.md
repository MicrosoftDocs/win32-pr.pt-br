---
description: O método EffectInsBefore insere um efeito no objeto no nível de prioridade especificado.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: 'Método IAMTimelineEffectable:: EffectInsBefore (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeca130f90cee5985f697a4efa042e3b4cb065b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789947"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>Método IAMTimelineEffectable:: EffectInsBefore

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `EffectInsBefore` método insere um efeito no objeto no nível de prioridade especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EffectInsBefore(
   IAMTimelineObj *pFX,
   long           Priority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFX* 
</dt> <dd>

Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do efeito.

</dd> <dt>

*Prioridade* 
</dt> <dd>

Nível de prioridade no qual inserir o efeito. Use o valor – 1 para inserir o efeito no final da lista de prioridades.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido ou E \_ NOTIMPL se o objeto não for um efeito. Caso contrário, retorna outro valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

As horas de início e de parada do efeito são recortadas dentro dos limites do intervalo de tempo do objeto, se necessário. Se já houver um efeito no nível de prioridade especificado, todos os efeitos desse ponto em mover para baixo na lista de prioridades para liberar espaço para o novo efeito.

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

[**Interface IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




