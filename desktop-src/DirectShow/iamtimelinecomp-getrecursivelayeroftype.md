---
description: O método GetRecursiveLayerOfType executa uma ordenação de profundidade das faixas virtuais contidas nessa composição e recupera a enésima faixa virtual a partir dessa ordem.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'Método IAMTimelineComp:: GetRecursiveLayerOfType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759552"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a>Método IAMTimelineComp:: GetRecursiveLayerOfType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetRecursiveLayerOfType` método executa uma ordenação de profundidade das faixas virtuais contidas nessa composição e recupera a *n* º de faixa virtual dessa ordem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppVirtualTrack* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do controle virtual.

</dd> <dt>

*WhichLayer* 
</dt> <dd>

Especifica qual faixa virtual deve ser recuperada, indexada a partir de zero.

</dd> <dt>

*Tipo* 
</dt> <dd>

Membro do tipo enumerado de [**\_ \_ tipo principal da linha do tempo**](timeline-major-type.md) que especifica se as faixas devem ser incluídas na pesquisa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos seguintes valores de **HRESULT** :



| Código de retorno                                                                                  | Descrição                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Nenhum objeto do tipo especificado.<br/> |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Argumento de ponteiro **nulo** .<br/>       |



 

## <a name="remarks"></a>Comentários

Normalmente, um aplicativo não precisará chamar esse método.

Se o parâmetro de *tipo* for linha de \_ \_ tipo principal \_ faixa, a ordenação de profundidade incluirá faixas. Caso contrário, ele inclui apenas composições e grupos. O objeto em si é incluído na ordenação.

Por exemplo, no arranjo a seguir, começando da composição A, a ordenação seria B, C, F, D, E, A.

![getrecursivelayeroftype](images/composition.png)

Se o método for executado com sucesso, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

 

 




