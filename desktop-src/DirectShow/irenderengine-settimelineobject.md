---
description: O método SetTimelineObject define a linha do tempo para o mecanismo de renderização usar.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: Método IRenderEngine::SetTimelineObject (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bb7862f247181d9aed6123e90507ed119594306a8d84be59ddd5204a816b33fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952485"
---
# <a name="irenderenginesettimelineobject-method"></a>Método IRenderEngine::SetTimelineObject

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetTimelineObject` método define a linha do tempo para o mecanismo de renderização usar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTimeline* 
</dt> <dd>

Ponteiro para a interface [**IAMTimeline**](iamtimeline.md) do objeto de linha do tempo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT:**



| Código de retorno                                                                                            | Descrição                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                            |
| <dl> <dt>**E \_ DEVE \_ INIT \_ RENDERER**</dt> </dl> | Falha na inicialização do mecanismo de renderização.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Memória insuficiente.<br/>                |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>              | Ponteiro inválido.<br/>                    |



 

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

[**IRenderEngine Interface**](irenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




