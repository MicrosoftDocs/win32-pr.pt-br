---
description: O método ClearProps limpa todos os dados de propriedade do setter de propriedade. O aplicativo pode definir novos dados de propriedade depois de chamar essa função.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: Método IPropertySetter::ClearProps (Qedit.h)
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
# <a name="ipropertysetterclearprops-method"></a>Método IPropertySetter::ClearProps

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ClearProps` método limpa todos os dados de propriedade do setter de propriedade. O aplicativo pode definir novos dados de propriedade depois de chamar essa função.

Limpar os dados da propriedade não restaura as propriedades do objeto para seus valores originais. Ele simplesmente impede que DirectShow aplicação de alterações posteriores. Os valores de propriedade são aplicados em tempo de operação quando o projeto é renderizar.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

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

 

 




