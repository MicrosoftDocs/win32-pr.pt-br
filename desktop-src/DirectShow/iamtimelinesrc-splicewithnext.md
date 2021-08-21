---
description: O método SpliceWithNext une o objeto de origem a outro objeto de origem.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'Método IAMTimelineSrc:: SpliceWithNext (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ffde9c7bb0416f2b296f7a7c347a058734430be33ef4ecde59e7e39cd6e845f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154827"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a>Método IAMTimelineSrc:: SpliceWithNext

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SpliceWithNext` método une o objeto de origem a outro objeto de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNext* 
</dt> <dd>

Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem para ingressar na fonte atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os possíveis valores de retorno incluem o seguinte:



| Código de retorno                                                                                   | Descrição                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento inválido.<br/>                                             |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | O objeto especificado pelo parâmetro *pNext* não é um objeto de origem.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Argumento de ponteiro **nulo** .<br/>                                    |



 

## <a name="remarks"></a>Comentários

Como implementado atualmente, esse método descarta todos os efeitos em *pNext*.

Para que esse método seja bem sucedido, *pNext* deve ser um quadro de correspondência do objeto de origem atual, definido da seguinte maneira:

-   Ele deve compartilhar o mesmo arquivo de origem.
-   A hora de início da mídia deve ser igual à hora de parada da mídia da origem atual.
-   A taxa de reprodução deve ser a mesma. A taxa de reprodução é a duração da mídia dividida pela duração da linha do tempo.

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

[**Interface IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




