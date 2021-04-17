---
description: O método GetCountOfType recupera o número de objetos de um determinado tipo contido nessa composição e todas as suas faixas virtuais, recursivamente.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'Método IAMTimelineComp:: GetCountOfType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754251"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>Método IAMTimelineComp:: GetCountOfType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetCountOfType` método recupera o número de objetos de um determinado tipo contido nessa composição e todas as suas faixas virtuais, recursivamente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recebe o número de objetos do tipo especificado contido nesta composição e todas as suas faixas virtuais, recursivamente.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Recebe a contagem retornada em *PVal* mais o número de composições pesquisadas, incluindo esta.

</dd> <dt>

*Majortype* 
</dt> <dd>

Membro do tipo enumerado de [**\_ \_ tipo principal da linha de tempo**](timeline-major-type.md) , especificando o tipo de objeto a ser contabilizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se for bem-sucedido ou o \_ ponteiro do contrário.

## <a name="remarks"></a>Comentários

Normalmente, um aplicativo não chamará esse método. Ele é chamado pelo mecanismo de processamento.

Se você contar as composições, o valor retornado em *PVal* será zero e o valor retornado em *pValWithComps* será o número de composições. O valor de *\* pValWithComps* inclui a composição na qual você chama o método. Por exemplo, se você chamar esse método em uma composição vazia, *\* pValWithComps* será igual a 1.

Os grupos não podem residir em composições, portanto, você não pode usar esse método para contar grupos. (A contagem retornada sempre será zero.) Para contar grupos, chame o método [**IAMTimeline:: GetGroupCount**](iamtimeline-getgroupcount.md) .

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

 

 




