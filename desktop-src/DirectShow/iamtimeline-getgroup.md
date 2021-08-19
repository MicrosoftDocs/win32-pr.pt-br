---
description: O método GetGroup recupera um grupo especificado.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: Método IAMTimeline::GetGroup (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71bf4aa0dd5d6f338da43d71384ead024fe821d3a639b0021299f6f6deb14be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685186"
---
# <a name="iamtimelinegetgroup-method"></a>Método IAMTimeline::GetGroup

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetGroup` método recupera um grupo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppGroup* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj do**](iamtimelineobj.md) grupo.

</dd> <dt>

*WhichGroup* 
</dt> <dd>

Índice do grupo a ser recuperado, com base na ordem em que os grupos foram adicionados à linha do tempo. O primeiro grupo adicionado à linha do tempo tem um índice de 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

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

[**IAMTimeline Interface**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




