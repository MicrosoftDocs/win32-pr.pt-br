---
title: Método SetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Define uma propriedade genérica de uma transferência de arquivo de otimização de entrega.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- Método SetProperty
- Método SetProperty, interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, método SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10da7fff9066ccefe7c356e3577ffffe7b0fc2e89d5fdb3f74611f5621d5b757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755596"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>Método IBackgroundCopyFile5:: SetProperty

Define uma propriedade genérica de uma transferência de arquivo de otimização de entrega.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PropertyId* \[ no\]
</dt> <dd>

Especifica a propriedade a ser definida.

</dd> <dt>

*ProertyValue* \[ fora\]
</dt> <dd>

Um ponteiro para uma União que especifica o valor a ser definido. O membro de União apropriado para a ID de propriedade é usado.

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

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





