---
description: O método GetOutputBuffering recupera o número de quadros processados antecipadamente durante a visualização.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: 'Método IAMTimelineGroup:: GetOutputBuffering (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 52917e798dcc71526f225fbca01038ee11c36c3c65fa1cebda88883ad2ae530e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428486"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a>Método IAMTimelineGroup:: GetOutputBuffering

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetOutputBuffering` método recupera o número de quadros renderizados antecipadamente durante a visualização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pnBuffer* \[ fora\]
</dt> <dd>

Recebe o número de quadros em buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

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

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




