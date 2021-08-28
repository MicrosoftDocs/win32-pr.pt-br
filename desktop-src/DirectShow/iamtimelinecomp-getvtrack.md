---
description: O método GetVTrack recupera a faixa virtual na prioridade especificada.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: Método IAMTimelineComp::GetVTrack (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 245f19783f7a472f86544d14f27c588e7a5938e899f2f389887d7a7817d6254e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756296"
---
# <a name="iamtimelinecompgetvtrack-method"></a>Método IAMTimelineComp::GetVTrack

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetVTrack` método recupera a faixa virtual na prioridade especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppVirtualTrack* \[ out\]
</dt> <dd>

Recebe a interface [**IAMTimelineObj**](iamtimelineobj.md) da faixa virtual.

</dd> <dt>

*Que* 
</dt> <dd>

Prioridade da faixa virtual a ser recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT:**



| Código de retorno                                                                                  | Descrição                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Nenhuma faixa virtual com a prioridade especificada.<br/> |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>    | Argumento de ponteiro **NULL.**<br/>                    |



 

## <a name="remarks"></a>Comentários

Se o método for bem-sucedido, a interface **IAMTimelineObj** retornada terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**IAMTimelineComp Interface**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




