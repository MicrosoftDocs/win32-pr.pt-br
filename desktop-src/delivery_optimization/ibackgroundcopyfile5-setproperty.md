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
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918356"
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

## <a name="return-value"></a>Retornar valor

Se esse método tiver sucesso, ele retornará **S_OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
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

 

 





