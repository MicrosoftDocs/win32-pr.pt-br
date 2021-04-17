---
description: O método GetProps recupera as propriedades definidas neste objeto, com seus valores correspondentes.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'Método IPropertySetter:: GetProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813086"
---
# <a name="ipropertysettergetprops-method"></a>Método IPropertySetter:: GetProps

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetProps` método recupera as propriedades definidas neste objeto, com seus valores correspondentes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcParams* \[ fora\]
</dt> <dd>

Recebe o número de estruturas retornadas em *paParam*.

</dd> <dt>

*paParam* \[ fora\]
</dt> <dd>

Endereço de um ponteiro para uma matriz de [**estruturas \_ param Dexter**](dexter-param.md) .

</dd> <dt>

*paValue* \[ fora\]
</dt> <dd>

Endereço de um ponteiro para uma matriz de estruturas de [**\_ valor Dexter**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Para cada propriedade retornada em *paParam*, o membro **nValores** indica o número de estruturas de [**\_ valor Dexter**](dexter-value.md) associadas à propriedade. Os pares são retornados em ordem de tempo crescente para cada propriedade.

Quando você terminar de usar as estruturas retornadas, chame [**IPropertySetter:: FreeProps**](ipropertysetter-freeprops.md) para liberar os recursos alocados por esse método.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como iterar por todos os valores em uma instância do setter de propriedade:


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




