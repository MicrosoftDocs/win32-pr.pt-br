---
description: O método EffectSwapPriorities alterna os níveis de prioridade de dois efeitos.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: Método IAMTimelineEffectable::EffectSwapPriorities (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e79f3f83422290600b4b6e75dbf15daff161f5e913a0300645254cdf94e7c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928226"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a>Método IAMTimelineEffectable::EffectSwapPriorities

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `EffectSwapPriorities` método alterna os níveis de prioridade de dois efeitos.

Dado dois valores de prioridade, esse método troca os efeitos nessas prioridades. Quando o método retorna, o efeito que estava no primeiro nível de prioridade está no segundo nível de prioridade e vice-versa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PriorityA* 
</dt> <dd>

Primeiro nível de prioridade no qual trocar efeitos.

</dd> <dt>

*PriorityB* 
</dt> <dd>

Segundo nível de prioridade no qual trocar efeitos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

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

 

 




