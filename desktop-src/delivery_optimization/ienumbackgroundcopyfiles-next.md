---
title: Método Next IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera um número especificado de itens na sequência de enumeração. Se houver menos do que o número solicitado de elementos restantes na sequência, ele recuperará os elementos restantes.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Próximo método
- Método Next, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, próximo método
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918926"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>Método IEnumBackgroundCopyFiles:: Next

Recupera um número especificado de itens na sequência de enumeração. Se houver menos do que o número solicitado de elementos restantes na sequência, ele recuperará os elementos restantes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*celt* \[ no\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*rgelt* \[ fora\]
</dt> <dd>

Matriz de objetos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) . Você deve liberar cada objeto em *rgelt* quando terminar.

</dd> <dt>

*pceltFetched* \[ fora\]
</dt> <dd>

Número de elementos retornados em *rgelt*. Você pode definir *pceltFetched* como **NULL** se *celt* for um. Caso contrário, inicialize o valor de *pceltFetched* como 0 antes de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                              | Descrição                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | O número de elementos solicitados foi retornado com êxito.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Retornou menos que o número de elementos solicitados.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





