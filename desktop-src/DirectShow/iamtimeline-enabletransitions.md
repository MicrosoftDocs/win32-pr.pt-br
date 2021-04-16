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
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752473"
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

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

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

 

 




