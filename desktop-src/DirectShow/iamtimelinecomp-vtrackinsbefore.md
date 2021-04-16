---
description: O método VTrackInsBefore insere uma faixa virtual na composição na prioridade especificada.
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'Método IAMTimelineComp:: VTrackInsBefore (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786976"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a>Método IAMTimelineComp:: VTrackInsBefore

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `VTrackInsBefore` método insere uma faixa virtual na composição na prioridade especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVirtualTrack* 
</dt> <dd>

Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) da faixa virtual.

</dd> <dt>

*Prioridade* 
</dt> <dd>

Prioridade na qual inserir a faixa virtual ou – 1 para inserir a faixa virtual no final da lista de prioridades. A lista de prioridades determina quais clipes são visíveis. Consulte comentários para obter mais informações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                   | Descrição                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Argumento inválido.<br/>              |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | O objeto não é uma faixa virtual.<br/> |



 

## <a name="remarks"></a>Comentários

Cada faixa virtual em composição tem um nível de prioridade exclusivo. Os níveis de prioridade variam de 0 a *n* -1, em que *n* é o número de faixas virtuais na composição. Para grupos de vídeos, uma faixa virtual oculta todas as faixas virtuais com um nível de prioridade mais baixo, exceto em locais onde a faixa está vazia ou contém uma transição. Você pode considerar as faixas virtuais como camadas na composição final. A faixa 1 está em camadas sobre o Track 0, o Track 2 é colocado em camadas na parte superior do Track 1 e assim por diante.

Se você especificar-1 para o parâmetro *Priority* , a faixa virtual será inserida no final da lista, com um valor de prioridade mais alto do que as faixas existentes. Se você especificar um valor de prioridade que já existe na composição, cada faixa com uma prioridade igual ou maior moverá um nível de prioridade acima.

**Exemplo**: Track A tem prioridade 0 e Track B tem prioridade 1. Se Track C for inserido na prioridade 0, Track a passa para a prioridade 1 e Track B passa para a prioridade 2.

Se a prioridade especificada for maior que o número atual de faixas na composição, o método falhará.

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

[**Interface IAMTimelineComp**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




