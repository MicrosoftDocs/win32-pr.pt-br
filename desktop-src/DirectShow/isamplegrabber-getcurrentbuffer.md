---
description: O método GetCurrentBuffer recupera uma cópia do buffer associado ao exemplo mais recente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: Método ISampleGrabber::GetCurrentBuffer (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 88af9469a1470a02be62b7684a66990c5622820e370518ed53267bd87d981879
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818045"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>Método ISampleGrabber::GetCurrentBuffer

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O **método GetCurrentBuffer** recupera uma cópia do buffer associado ao exemplo mais recente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBufferSize* \[ in, out\]
</dt> <dd>

Ponteiro para o tamanho do buffer. Se *pBuffer* for **NULL,** esse parâmetro receberá o tamanho do buffer necessário, em bytes. Se *pBuffer* não for **NULL,** de definido esse parâmetro igual ao tamanho do buffer, em bytes. Na saída, o parâmetro recebe o número de bytes que foram copiados para o buffer. Esse valor pode ser menor que o tamanho do buffer.

</dd> <dt>

*pBuffer* \[ out\]
</dt> <dd>

Ponteiro para uma matriz de bytes de tamanho *pBufferSize* ou **NULL.** Se esse parâmetro não for **NULL,** o buffer atual será copiado para a matriz. Se esse parâmetro for **NULL,** o *parâmetro pBufferSize* receberá o tamanho do buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores a seguir.



| Código de retorno                                                                                           | Descrição                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Os exemplos não estão sendo armazenados em buffer. Chame [**ISampleGrabber::SetBufferSamples.**](isamplegrabber-setbuffersamples.md)<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | O buffer especificado não é grande o suficiente.<br/>                                                                         |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>             | Argumento de ponteiro **NULL.**<br/>                                                                                        |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | O filtro não está conectado.<br/>                                                                                      |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ ERRADO**</dt> </dl>   | O filtro ainda não recebeu amostras. Para fornecer um exemplo, execute ou pause o grafo.<br/>                         |



 

## <a name="remarks"></a>Comentários

Para ativar o buffer, chame [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) com um valor **true.**

Chame esse método duas vezes. Na primeira chamada, de definir *pBuffer* como **NULL.** O tamanho do buffer é retornado em *pBufferSize.* Em seguida, aloce uma matriz e chame o método novamente. Na segunda chamada, passe o tamanho da matriz em *pBufferSize* e passe o endereço da matriz em *pBuffer*. Se a matriz não for grande o suficiente, o método retornará E \_ OUTOFMEMORY.

O *parâmetro pBuffer* é digitado como um **ponteiro longo,** mas o conteúdo do buffer depende do formato dos dados. Chame [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) para obter o tipo de mídia do formato.

Não chame esse método enquanto o grafo de filtro estiver em execução. Enquanto o grafo de filtro está em execução, o filtro Grabber de Exemplo substitui o conteúdo do buffer sempre que ele recebe um novo exemplo. A melhor maneira de usar esse método é usar o "modo de disparo único", que interrompe o grafo depois de receber a primeira amostra. Para definir o modo de captura única, chame [**ISampleGrabber::SetOneShot.**](isamplegrabber-setoneshot.md)

O filtro não buffer de exemplos de pré-roll ou amostras em que o **membro dwStreamId** da estrutura [**AM \_ SAMPLE2 \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) é algo diferente de AM \_ STREAM \_ MEDIA.

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

 

 




