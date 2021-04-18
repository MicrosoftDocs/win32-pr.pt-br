---
description: O método CloneProps clona um conjunto de propriedades desse setter de propriedade e as adiciona a um novo setter de propriedade.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'Método IPropertySetter:: CloneProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760184"
---
# <a name="ipropertysettercloneprops-method"></a>Método IPropertySetter:: CloneProps

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `CloneProps` método clona um conjunto de propriedades deste setter de propriedade e os adiciona a um novo setter de propriedade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSetter* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface **IPropertySetter** do setter da nova propriedade.

</dd> <dt>

*rtStart* \[ no\]
</dt> <dd>

Hora de início do intervalo de valores a serem clonados, em unidades de 100 a nanossegundos.

</dd> <dt>

*rtStop* \[ no\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Somente os valores que se enquadram após a hora de início especificada são clonados. Os horários nos valores clonados são então ajustados em relação à hora de início. Por exemplo, se *rtStart* for 20 milhões (2 segundos), um valor na hora 30 milhões (3 segundos) será clonado com o tempo 10 milhões (1 segundo). Por fim, cada propriedade clonada recebe um valor inicial igual ao valor da propriedade original na hora de início (interpolada corretamente, se necessário). Na verdade, os dados da propriedade são divididos na hora de início especificada.

Se o método for executado com sucesso, a interface [**IPropertySetter**](ipropertysetter.md) que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




