---
description: O método gettimelineobject recupera a linha do tempo que o mecanismo de processamento está usando no momento.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'Método IRenderEngine:: gettimelineobject (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c21868dc705a5c9f3b40649540fcaadb1f9219a7443d58c59964606cb7ed7d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823356"
---
# <a name="irenderenginegettimelineobject-method"></a>Método IRenderEngine:: gettimelineobject

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetTimelineObject` método recupera a linha do tempo que o mecanismo de processamento está usando no momento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppTimeline* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimeline**](iamtimeline.md) da linha do tempo. Ele receberá o valor **NULL** se não houver linha do tempo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                            | Descrição                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Êxito.<br/>                            |
| <dl> <dt>**\_ponteiro E**</dt> </dl>              | Ponteiro inválido.<br/>                    |
| <dl> <dt>**E \_ deve \_ iniciar o \_ renderizador**</dt> </dl> | Falha ao inicializar o mecanismo de renderização.<br/> |



 

## <a name="remarks"></a>Comentários

No retorno, se o valor de *\* ppTimeline* for não **nulo**, a interface **IAMTimeline** terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




