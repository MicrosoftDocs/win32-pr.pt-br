---
description: O método GetCountOfType recupera o número de objetos de um determinado tipo contidos nessa composição e todas as suas faixas virtuais, recursivamente.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: Método IAMTimelineComp::GetCountOfType (Qedit.h)
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
ms.openlocfilehash: b0504a7adb41a0d6a45714090a39aeefda9a3ef53b2d834540f600ec3ef871a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756406"
---
# <a name="iamtimelinecompgetcountoftype-method"></a>Método IAMTimelineComp::GetCountOfType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método recupera o número de objetos de um determinado tipo contidos nessa composição e todas as suas `GetCountOfType` faixas virtuais, recursivamente.

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

*Pval* 
</dt> <dd>

Recebe o número de objetos do tipo especificado contidos nessa composição e todas as suas faixas virtuais, recursivamente.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Recebe a contagem retornada em *pVal* mais o número de composições pesquisadas, incluindo esta.

</dd> <dt>

*MajorType* 
</dt> <dd>

Membro do tipo [**enumerado TIMELINE \_ MAJOR \_ TYPE,**](timeline-major-type.md) especificando o tipo de objeto a ser contado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se for bem-sucedido ou E \_ POINTER caso contrário.

## <a name="remarks"></a>Comentários

Normalmente, um aplicativo não chamará esse método. Ele é chamado pelo mecanismo de renderização.

Se você contar composições, o valor retornado em *pVal* será zero e o valor retornado em *pValWithComps* será o número de composições. O valor de *\* pValWithComps* inclui a composição na qual você chama o método . Por exemplo, se você chamar esse método em uma composição vazia, *\* pValWithComps* será igual a 1.

Os grupos não podem residir dentro de composições, portanto, você não pode usar esse método para contar grupos. (A contagem retornada sempre será zero.) Para contar grupos, chame o [**método IAMTimeline::GetGroupCount.**](iamtimeline-getgroupcount.md)

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

[**IAMTimelineComp Interface**](iamtimelinecomp.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




