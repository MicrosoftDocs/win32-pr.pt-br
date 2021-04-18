---
description: O método GetCountOfType recupera o número de objetos do tipo especificado que estão contidos em um grupo especificado e todos os seus filhos.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'Método IAMTimeline:: GetCountOfType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751873"
---
# <a name="iamtimelinegetcountoftype-method"></a>Método IAMTimeline:: GetCountOfType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetCountOfType` método recupera o número de objetos do tipo especificado que estão contidos em um grupo especificado e todos os seus filhos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Grupo* 
</dt> <dd>

Número de índice do grupo para o qual a contagem será recuperada.

</dd> <dt>

*pVal* 
</dt> <dd>

Recebe o número de objetos do tipo especificado contido no grupo e todas as suas faixas virtuais, recursivamente.

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

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                  | Descrição                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Número de grupo inválido.<br/>      |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo** .<br/> |



 

## <a name="remarks"></a>Comentários

Chamar esse método é equivalente a chamar [**IAMTimelineComp:: GetCountOfType**](iamtimelinecomp-getcountoftype.md) no grupo especificado. Consulte a seção comentários desse método para obter mais informações.

Normalmente, um aplicativo não chamará esse método. Ele é chamado internamente pelo mecanismo de processamento.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




