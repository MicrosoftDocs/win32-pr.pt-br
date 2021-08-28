---
description: 'O método InsertSpace2 divide todos os objetos que existem no tempo especificado e insere um espaço entre eles. Esse método é equivalente a IAMTimelineTrack:: InsertSpace, mas usa os valores de REFTIME.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'Método IAMTimelineTrack:: InsertSpace2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f851e6bdccb755977210fcd67e7ce0bb6cb270ec3ff6a4f1fed4806a035a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052246"
---
# <a name="iamtimelinetrackinsertspace2-method"></a>Método IAMTimelineTrack:: InsertSpace2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `InsertSpace2` método divide todos os objetos existentes na hora especificada e insere o espaço entre eles. Esse método é equivalente a [**IAMTimelineTrack:: InsertSpace**](iamtimelinetrack-insertspace.md), mas usa os valores de [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtStart* 
</dt> <dd>

Hora na qual criar a divisão e o ponto inicial do espaço inserido, em segundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Ponto de extremidade do espaço inserido, em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores de retorno incluem o seguinte:



| Código de retorno                                                                                   | Descrição                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>       | Não há objetos no horário especificado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento inválido.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>                        |



 

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

 

 




