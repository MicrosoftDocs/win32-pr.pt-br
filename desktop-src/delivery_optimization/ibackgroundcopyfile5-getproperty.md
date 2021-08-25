---
title: Método GetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Obtém uma propriedade genérica de uma transferência de arquivo de otimização de entrega.
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- Método GetProperty
- Método GetProperty, interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, método GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a664c752bd28b176189cdd77e955684236cfa23c6b384378610336335651fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635946"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a>Método IBackgroundCopyFile5:: GetProperty

Obtém uma propriedade genérica de uma transferência de arquivo de otimização de entrega.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PropertyId* \[ no\]
</dt> <dd>

Especifica a propriedade de arquivo cujo valor deve ser recuperado.

</dd> <dt>

*PropertyValue* \[ fora\]
</dt> <dd>

O valor da propriedade, retornado como um ponteiro para uma BITS_FILE_PROPERTY_VALUE Union. Use o campo Union apropriado para o valor de ID de propriedade passado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método tiver sucesso, ele retornará **S_OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 é definido como 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





