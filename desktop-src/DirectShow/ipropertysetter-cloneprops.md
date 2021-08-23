---
description: O método CloneProps clona um conjunto de propriedades dessa propriedade setter e as adiciona a um novo setter de propriedade.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: Método IPropertySetter::CloneProps (Qedit.h)
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
ms.openlocfilehash: 54dd2ad08334a0c61918de74396e62fcc21e095df81c2d773995b6cfbdddc19d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755916"
---
# <a name="ipropertysettercloneprops-method"></a>Método IPropertySetter::CloneProps

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `CloneProps` método clona um conjunto de propriedades desse setter de propriedade e as adiciona a um novo setter de propriedade.

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

*ppSetter* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface **IPropertySetter** do novo setter de propriedade.

</dd> <dt>

*rtStart* \[ Em\]
</dt> <dd>

Hora de início do intervalo de valores a clonar, em unidades de 100 nanossegundos.

</dd> <dt>

*rtStop* \[ Em\]
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Somente os valores que se enquadram após a hora de início especificada são clonados. As horas nos valores clonados são ajustadas em relação à hora de início. Por exemplo, se *rtStart* for 20000000 (2 segundos), um valor no momento 300000000 (3 segundos) será clonado com o tempo 100000000 (1 segundo). Por fim, cada propriedade clonada recebe um valor inicial igual ao valor da propriedade original na hora de início (interpolada corretamente, se necessário). Na verdade, os dados da propriedade são divididos na hora de início especificada.

Se o método for bem-sucedido, a interface [**IPropertySetter**](ipropertysetter.md) retornada terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

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

[**IPropertySetter Interface**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




