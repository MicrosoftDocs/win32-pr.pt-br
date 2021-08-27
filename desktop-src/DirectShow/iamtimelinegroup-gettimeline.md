---
description: O método gettimen recupera a linha do tempo à qual esse grupo pertence.
ms.assetid: a57d75c9-6e2e-426f-9403-ad32188b2211
title: 'Método IAMTimelineGroup:: gettimeize (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: da9064969cc026ebffb91ccbdb70bcaebab2b5d696bcb04d6c6281548721c522
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086836"
---
# <a name="iamtimelinegroupgettimeline-method"></a>Método IAMTimelineGroup:: gettimen

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetTimeline` método recupera a linha do tempo à qual esse grupo pertence.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTimeline(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppTimeline* \[ fora\]
</dt> <dd>

Recebe a interface [**IAMTimeline**](iamtimeline.md) da linha do tempo. Se o grupo não fizer parte de uma linha do tempo, o valor será definido como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Se o valor retornado em *ppTimeline* não for **NULL**, a interface **IAMTimeline** terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

 

 




