---
description: O método EffectInsBefore insere um efeito no objeto no nível de prioridade especificado.
ms.assetid: 6c98e24a-5bac-4273-ae3c-2ab3c9d9465b
title: Método IAMTimelineEffectable::EffectInsBefore (Qedit.h)
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
ms.openlocfilehash: 0eca93a6c1837b8a7a8f5a95a6cdbf9e87f99191c0911a82e6fd7a3586eb8c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052746"
---
# <a name="iamtimelineeffectableeffectinsbefore-method"></a>Método IAMTimelineEffectable::EffectInsBefore

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

*Pfx* 
</dt> <dd>

Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do efeito.

</dd> <dt>

*Prioridade* 
</dt> <dd>

Nível de prioridade no qual inserir o efeito. Use o valor –1 para inserir o efeito no final da lista de prioridade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou E \_ NOTIMPL se o objeto não for um efeito. Caso contrário, retornará **outro valor HRESULT** indicando a causa do erro.

## <a name="remarks"></a>Comentários

Os horários de início e parada do efeito são recortados dentro dos limites do intervalo de tempo do objeto, se necessário. Se já houver um efeito no nível de prioridade especificado, todos os efeitos desse ponto em diante movem para baixo a lista de prioridade para dar espaço para o novo efeito.

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

[**IAMTimelineEffectable Interface**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




