---
description: O método EnableTransitions habilita ou desabilita todas as transições na linha do tempo.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'Método IAMTimeline:: EnableTransitions (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9356ac53488f68e54a05a85e8e287850138ee131f80dd3bb45b81cf606b5a351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401067"
---
# <a name="iamtimelineenabletransitions-method"></a>Método IAMTimeline:: EnableTransitions

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `EnableTransitions` método habilita ou desabilita todas as transições na linha do tempo. Se as transições estiverem desabilitadas, os mecanismos de renderização as tratarão como cortes; ou seja, a saída renderizada salta instantaneamente de uma faixa para a próxima. O ponto de recorte padrão é a metade da duração da transição. Você pode alterar o ponto de recorte chamando o método [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md) na transição. As transições desabilitadas não são removidas da linha do tempo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fEnabled* 
</dt> <dd>

Valor booliano que especifica se as transições devem ser habilitadas ou desabilitadas. Se **for true**, as transições serão habilitadas. Se **for false**, as transições serão desabilitadas.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




