---
description: O método SetCallback especifica um método de retorno de chamada para chamar em exemplos de entrada.
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'Método ISampleGrabber:: SetCallback (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810169"
---
# <a name="isamplegrabbersetcallback-method"></a>Método ISampleGrabber:: SetCallback

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método **SetCallback** especifica um método de retorno de chamada para chamar em exemplos de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCallback* 
</dt> <dd>

Ponteiro para uma interface [**ISampleGrabberCB**](isamplegrabbercb.md) que contém o método de retorno de chamada ou **nulo** para cancelar o retorno de chamada.

</dd> <dt>

*WhichMethodToCallback* 
</dt> <dd>

Índice que especifica o método de retorno de chamada. Deve ser um dos valores a seguir.



| Valor | Descrição                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | O filtro de apoio de exemplo chama o método [**ISampleGrabberCB:: SampleCB**](isamplegrabbercb-samplecb.md) . Esse método recebe um ponteiro [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .               |
| 1     | O filtro de apoio de exemplo chama o método [**ISampleGrabberCB:: BufferCB**](isamplegrabbercb-buffercb.md) . Esse método recebe um ponteiro para o buffer que está contido no exemplo de mídia. |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O thread de processamento de dados é bloqueado até que o método de retorno de chamada seja retornado. Se o retorno de chamada não retornar rapidamente, ele poderá interferir na reprodução.

O filtro não invoca a função de retorno de chamada para exemplos de prelance ou para exemplos nos quais o membro **dwStreamId** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) é algo diferente da \_ mídia de fluxo am \_ .

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

[Usando o exemplo de apoio](using-the-sample-grabber.md)
</dt> <dt>

[**Interface ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




