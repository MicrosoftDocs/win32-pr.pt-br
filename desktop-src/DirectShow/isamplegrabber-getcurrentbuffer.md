---
description: O método GetCurrentBuffer recupera uma cópia do buffer associado ao exemplo mais recente.
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'Método ISampleGrabber:: GetCurrentBuffer (QEdit. h)'
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
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766303"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a>Método ISampleGrabber:: GetCurrentBuffer

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método **GetCurrentBuffer** recupera uma cópia do buffer associado ao exemplo mais recente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pBufferSize* \[ entrada, saída\]
</dt> <dd>

Ponteiro para o tamanho do buffer. Se *pBuffer* for **NULL**, esse parâmetro receberá o tamanho de buffer necessário, em bytes. Se *pBuffer* não for **NULL**, defina esse parâmetro como igual ao tamanho do buffer, em bytes. Na saída, o parâmetro recebe o número de bytes que foram copiados no buffer. Esse valor pode ser menor do que o tamanho do buffer.

</dd> <dt>

*pBuffer* \[ fora\]
</dt> <dd>

Ponteiro para uma matriz de bytes de tamanho *pBufferSize* ou **NULL**. Se esse parâmetro não for **nulo**, o buffer atual será copiado para a matriz. Se esse parâmetro for **nulo**, o parâmetro *pBufferSize* receberá o tamanho de buffer necessário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores a seguir.



| Código de retorno                                                                                           | Descrição                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Os exemplos não estão sendo armazenados em buffer. Chame [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md).<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | O buffer especificado não é grande o suficiente.<br/>                                                                         |
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Argumento de ponteiro **nulo** .<br/>                                                                                        |
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                                                                                                          |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O filtro não está conectado.<br/>                                                                                      |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl>   | O filtro ainda não recebeu amostras. Para entregar um exemplo, execute ou Pause o grafo.<br/>                         |



 

## <a name="remarks"></a>Comentários

Para ativar o buffer, chame [**ISampleGrabber:: SetBufferSamples**](isamplegrabber-setbuffersamples.md) com um valor de **true**.

Chame esse método duas vezes. Na primeira chamada, defina *pBuffer* como **nulo**. O tamanho do buffer é retornado em *pBufferSize*. Em seguida, aloque uma matriz e chame o método novamente. Na segunda chamada, passe o tamanho da matriz em *pBufferSize* e passe o endereço da matriz em *pBuffer*. Se a matriz não for grande o suficiente, o método retornará E \_ OUTOFMEMORY.

O parâmetro *pBuffer* é digitado como um ponteiro **longo** , mas o conteúdo do buffer depende do formato dos dados. Chame [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) para obter o tipo de mídia do formato.

Não chame esse método enquanto o grafo de filtro estiver em execução. Enquanto o grafo de filtro está em execução, o filtro de apoio de exemplo substitui o conteúdo do buffer sempre que recebe um novo exemplo. A melhor maneira de usar esse método é usar o "modo One-shot", que interrompe o grafo depois de receber o primeiro exemplo. Para definir o modo One-shot, chame [**ISampleGrabber:: SetOneShot**](isamplegrabber-setoneshot.md).

O filtro não armazena amostras de registro em buffer ou exemplos em que o membro **dwStreamId** da estrutura [**de \_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) é algo diferente da mídia de fluxo am \_ \_ .

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

 

 




