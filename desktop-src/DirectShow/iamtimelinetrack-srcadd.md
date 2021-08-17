---
description: O método SrcAdd adiciona uma origem à faixa.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: Método IAMTimelineTrack::SrcAdd (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e705f840a073ee6796776f6f68c7b57df0bd972facf8f7a586792519735bfb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998746"
---
# <a name="iamtimelinetracksrcadd-method"></a>Método IAMTimelineTrack::SrcAdd

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SrcAdd` método adiciona uma origem à faixa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Psrc* 
</dt> <dd>

Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido. Retornará E \_ NOINTERFACE se o objeto não for um objeto de origem. Caso contrário, retornará **um valor HRESULT** indicando a causa do erro.

## <a name="remarks"></a>Comentários

De definir os horários de início e de parada da origem antes de chamar esse método. (Chame [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md).)

Atualmente, o DES não pode renderizar simultaneamente mais de 75 fontes que foram compactadas com codecs do VCM (Gerenciador de Compactação de Vídeo). Além disso, se o projeto como um todo contiver mais de 75 dessas fontes, você deverá usar a reconexão dinâmica ou o DES não poderá visualizar o projeto. Para obter mais informações, [**consulte IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

 

 




