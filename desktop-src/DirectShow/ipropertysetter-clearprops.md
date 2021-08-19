---
description: O método ClearProps limpa todos os dados de Propriedade do setter de propriedade. O aplicativo pode definir novos dados de propriedade depois de chamar essa função.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'Método IPropertySetter:: ClearProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dfe5db4d7ae1f4a2d7a070a3d735264e61dfbdb621f99b9cbb2e1040213b56c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818585"
---
# <a name="ipropertysetterclearprops-method"></a>Método IPropertySetter:: ClearProps

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ClearProps` método limpa todos os dados de Propriedade do setter de propriedade. O aplicativo pode definir novos dados de propriedade depois de chamar essa função.

Limpar os dados de propriedade não restaura as propriedades do objeto para seus valores originais. ele simplesmente impede que DirectShow apliquem outras alterações. Os valores de propriedade são aplicados em tempo de execução quando o projeto é renderizado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

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

 

 




