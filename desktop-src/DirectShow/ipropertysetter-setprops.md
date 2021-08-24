---
description: O método SetProps define as propriedades do objeto de destino para o estado apropriado para o tempo especificado.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: Método IPropertySetter::SetProps (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b3b5a1832897b52d21c57e26595b7d66c4fc9a53f2bcbee0090c53d00f8fe832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767206"
---
# <a name="ipropertysettersetprops-method"></a>Método IPropertySetter::SetProps

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetProps` método define as propriedades do objeto de destino para o estado apropriado para o tempo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTarget* \[ Em\]
</dt> <dd>

Ponteiro para o objeto de destino para o qual definir as propriedades.

</dd> <dt>

*rtNow* \[ Em\]
</dt> <dd>

Hora em que definir as propriedades, em unidades de 100 nanossegundos ou –1 para definir propriedades estáticas (aquelas que não variam ao longo do tempo).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método é chamado pelo DES para definir as propriedades em uma transição ou efeito. Um aplicativo normalmente não chamará esse método.

O objeto especificado por *pTarget* deve implementar a interface **IDispatch.**

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

 

 




