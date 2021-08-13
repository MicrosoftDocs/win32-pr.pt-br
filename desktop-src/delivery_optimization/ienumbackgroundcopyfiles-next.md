---
title: Método IEnumBackgroundCopyFiles Next (Deliveryoptimization.h)
description: Recupera um número especificado de itens na sequência de enumeração. Se houver menos do que o número solicitado de elementos restantes na sequência, ele recuperará os elementos restantes.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Próximo método
- Próximo método, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, método Next
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
ms.openlocfilehash: 3dcf24c65b7f282b1a1e15d3109ce1af9ccfc0af6436c80c94760f0b4cd18069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461876"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>Método IEnumBackgroundCopyFiles::Next

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

*ao mesmo tempo* \[ Em\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Matriz de [**objetos IBackgroundCopyFile.**](ibackgroundcopyfile.md) Você deve liberar cada objeto em *rgelt* quando terminar.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Número de elementos retornados *em rgelt*. Você poderá definir *pceltFetched como* **NULL** se *for* um. Caso contrário, inicialize o valor *de pceltFetched* como 0 antes de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os seguintes **valores HRESULT,** bem como outros.



| Código de retorno                                                                              | Descrição                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Retornou com êxito o número de elementos solicitados.<br/> |
| <dl> <dt>**S_false**</dt> </dl>  | Retornado menor que o número de elementos solicitados.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





