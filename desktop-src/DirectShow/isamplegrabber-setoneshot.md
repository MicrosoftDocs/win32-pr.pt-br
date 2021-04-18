---
description: O método SetOneShot especifica se o filtro de apoio de exemplo é interrompido depois que o filtro recebe um exemplo.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'Método ISampleGrabber:: SetOneShot (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757010"
---
# <a name="isamplegrabbersetoneshot-method"></a>Método ISampleGrabber:: SetOneShot

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método **SetOneShot** especifica se o filtro de [**apoio de exemplo**](sample-grabber-filter.md) é interrompido depois que o filtro recebe um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OneShot* 
</dt> <dd>

Um valor booliano que especifica se o filtro de apoio de exemplo é interrompido depois de receber um exemplo.



| Valor                                                                                                                                    | Significado                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>VERDADEIRO * * * *</dt> </dl>    | O exemplo de apoio é interrompido após o primeiro exemplo. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Após o primeiro exemplo, o exemplo de apoio continua a processar exemplos. Esse é o comportamento padrão.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Use este método para obter uma única amostra do fluxo, da seguinte maneira:

1.  Chame **SetOneShot** com o valor **true**.
2.  Opcionalmente, use a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) para buscar uma posição no fluxo.
3.  Chame [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) para executar o gráfico de filtro.
4.  Chame [**IMediaEvent:: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) para aguardar a parada do grafo. Como alternativa, chame [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obter eventos de grafo, até que você receba o evento [**EC \_ Complete**](ec-complete.md) .

Depois que o exemplo de apoio for interrompido, o gráfico de filtro ainda estará em estado de execução. Você pode buscar ou pausar o grafo para obter outra amostra.

> [!Note]  
> Uma versão anterior da documentação declarava que o gráfico de filtro é interrompido depois que o exemplo é recebido. Isso não é preciso. O fluxo termina, mas o grafo permanece no estado executando.

 

O exemplo de apoio implementa o modo One-Shot chamando [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no filtro downstream e retornando S \_ false do método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) dele.

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

 

 




