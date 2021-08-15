---
description: O método InsertSpace divide todos os objetos que existem no momento especificado e insere espaço entre eles.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: Método IAMTimelineTrack::InsertSpace (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a51e89a72d813e1f5a9c1c05b1a46b6674906284b61b4036c164af87af9a4559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399173"
---
# <a name="iamtimelinetrackinsertspace-method"></a>Método IAMTimelineTrack::InsertSpace

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método divide todos os objetos que existem no momento especificado e `InsertSpace` insere espaço entre eles.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtStart* 
</dt> <dd>

Hora na qual criar a divisão e o ponto inicial do espaço inserido, em unidades de 100 nanossegundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Ponto final do espaço inserido, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores de retorno incluem o seguinte:



| Código de retorno                                                                                   | Description                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Não há objetos no momento especificado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento inválido.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>                        |



 

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

[**IAMTimelineTrack Interface**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




