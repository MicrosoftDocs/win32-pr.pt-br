---
description: O método SrcAdd adiciona uma origem à faixa.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'Método IAMTimelineTrack:: SrcAdd (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780054"
---
# <a name="iamtimelinetracksrcadd-method"></a>Método IAMTimelineTrack:: SrcAdd

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SrcAdd` método adiciona uma origem à faixa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrc* 
</dt> <dd>

Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará S \_ OK se for bem-sucedido. Retorna E \_ nointerface se o objeto não for um objeto de origem. Caso contrário, retorna um valor **HRESULT** que indica a causa do erro.

## <a name="remarks"></a>Comentários

Defina as horas de início e de término da origem antes de chamar esse método. (Chamar [**IAMTimelineObj:: SetStartStop**](iamtimelineobj-setstartstop.md).)

Atualmente, o DES não pode renderizar simultaneamente mais de 75 fontes que foram compactadas com codecs do VCM (Gerenciador de compactação de vídeo). Além disso, se o projeto como um todo contiver mais de 75 fontes, você deverá usar a reconexão dinâmica ou o DES não poderá visualizar o projeto. Para obter mais informações, consulte [**IRenderEngine:: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).

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

[**Interface IAMTimelineTrack**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




