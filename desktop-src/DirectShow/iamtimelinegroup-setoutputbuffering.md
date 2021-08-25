---
description: O método SetOutputBuffering especifica o número de quadros renderizados antecipadamente durante a visualização.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'Método IAMTimelineGroup:: SetOutputBuffering (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8187918a4f6d04df9c8c0eaff387a092f18181071ce6ba41c83de44fcb095bbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915186"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>Método IAMTimelineGroup:: SetOutputBuffering

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetOutputBuffering` método especifica o número de quadros renderizados antecipadamente durante a visualização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nBuffer* \[ no\]
</dt> <dd>

Número de quadros para armazenar em buffer durante a visualização. Deve ser dois ou mais.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Um buffer maior requer mais memória, mas pode resultar em uma visualização mais suave, especialmente durante efeitos ou transições que exigem mais tempo para serem renderizados. O buffer padrão é de 30 quadros.

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




