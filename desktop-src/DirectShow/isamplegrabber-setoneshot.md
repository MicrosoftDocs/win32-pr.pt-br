---
description: O método SetOneShot especifica se o filtro Grabber de Exemplo é interrompido depois que o filtro recebe um exemplo.
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: Método ISampleGrabber::SetOneShot (Qedit.h)
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
ms.openlocfilehash: 7829bd57cb2d813f71e17a4925d6e5fab7cc34330041461b691e00eae6ca5cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817677"
---
# <a name="isamplegrabbersetoneshot-method"></a>Método ISampleGrabber::SetOneShot

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O **método SetOneShot** especifica se o filtro [**Grabber de**](sample-grabber-filter.md) Exemplo é interrompido depois que o filtro recebe um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Oneshot* 
</dt> <dd>

Um valor booliana que especifica se o filtro Grabber de Exemplo é interrompido depois de receber uma amostra.



| Valor                                                                                                                                    | Significado                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE****</dt> </dl>    | O Exemplo de Grabber é interrompido após o primeiro exemplo. <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE****</dt> </dl> | Após o primeiro exemplo, o Exemplo de Grabber continua a processar exemplos. Esse é o comportamento padrão.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Use esse método para obter um único exemplo do fluxo, da seguinte forma:

1.  Chame **SetOneShot** com o valor **TRUE.**
2.  Opcionalmente, use a interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) para buscar uma posição no fluxo.
3.  Chame [**IMediaControl::Run para**](/windows/desktop/api/Control/nf-control-imediacontrol-run) executar o grafo de filtro.
4.  Chame [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) para aguardar a interrupção do grafo. Como alternativa, chame [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) para obter eventos de grafo até receber o [**evento EC \_ COMPLETE.**](ec-complete.md)

Depois que o Sample Grabber for interrompido, o grafo de filtro ainda está em um estado de execução. Você pode buscar ou pausar o grafo para obter outro exemplo.

> [!Note]  
> Uma versão anterior da documentação declarou que o grafo de filtro é interrompido depois que o exemplo é recebido. Isso não é preciso. O fluxo termina, mas o grafo permanece no estado de execução.

 

O Exemplo de Grabber implementa o modo de captura única chamando [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no filtro downstream e retornando S FALSE do método \_ [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) dele.

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

[Usando o exemplo de grabber](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber Interface**](isamplegrabber.md)
</dt> </dl>

 

 




