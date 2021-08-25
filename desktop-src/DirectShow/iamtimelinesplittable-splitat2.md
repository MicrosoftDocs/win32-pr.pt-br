---
description: 'O método SplitAt2 divide o objeto na hora especificada. Esse método é equivalente a IAMTimelineSplittable:: SplitAt, mas usa um valor de REFTIME.'
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'Método IAMTimelineSplittable:: SplitAt2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9c3a5720ade42291037611c155c2cb9e834f0734e7af6e2c36277c409592143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904906"
---
# <a name="iamtimelinesplittablesplitat2-method"></a>Método IAMTimelineSplittable:: SplitAt2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SplitAt2` método divide o objeto na hora especificada. Esse método é equivalente a [**IAMTimelineSplittable:: SplitAt**](iamtimelinesplittable-splitat.md), mas usa um valor de [**REFTIME**](reftime.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hora* 
</dt> <dd>

Hora na qual dividir o objeto, em relação ao início da linha do tempo, em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                   | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>       | Nada para dividir.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O objeto não existe no momento.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>                    |



 

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

[**Interface IAMTimelineSplittable**](iamtimelinesplittable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




