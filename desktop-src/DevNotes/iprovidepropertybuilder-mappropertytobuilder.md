---
description: Verifica se um construtor deve ser associado a uma determinada propriedade.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'Método IProvidePropertyBuilder:: MapPropertyToBuilder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753062"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>Método IProvidePropertyBuilder:: MapPropertyToBuilder

Verifica se um construtor deve ser associado a uma determinada propriedade.

## <a name="syntax"></a>Sintaxe


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DISPID* \[ no\]
</dt> <dd>

O DISPID da propriedade em questão.

</dd> <dt>

*pdwCtlBldType* \[ fora\]
</dt> <dd>

O Construtor a ser mapeado. Esse parâmetro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                                          | Significado                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt> </dl>    | Invocar um Standard Builder do sistema (sem suporte no Visual Studio).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt> </dl> | Invocar um construtor personalizado.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt> </dl> | O Construtor modifica o objeto. Esse comportamento é comum.<br/>              |



 

</dd> <dt>

*pbstrGuidBldr* \[ fora\]
</dt> <dd>

O GUID que identifica o construtor para essa propriedade.

</dd> <dt>

*builderAvailable* \[ out, retval\]
</dt> <dd>

Esse parâmetro será **true** se essa propriedade atualmente der suporte a um construtor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




