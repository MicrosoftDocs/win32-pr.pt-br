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
ms.openlocfilehash: 6e6d61d60a4664386cded025d2b7bcea82353602c7f7f8c0fb5bc4c53779ae2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817913"
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

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O thread de processamento de dados é bloqueado até que o método de retorno de chamada seja retornado. Se o retorno de chamada não retornar rapidamente, ele poderá interferir na reprodução.

O filtro não invoca a função de retorno de chamada para exemplos de prelance ou para exemplos nos quais o membro **dwStreamId** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) é algo diferente da \_ mídia de fluxo am \_ .

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

[Usando o exemplo de apoio](using-the-sample-grabber.md)
</dt> <dt>

[**Interface ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




