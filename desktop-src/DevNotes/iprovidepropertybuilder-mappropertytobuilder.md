---
description: Verifica se um construtor deve ser associado a uma propriedade específica.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: Método IProvidePropertyBuilder::MapPropertyToBuilder
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
ms.openlocfilehash: 35ff9e82164251c4490355bbf0499b7fa690415d388b95f7f9c7fd0e6bd7dd3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001686"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a>Método IProvidePropertyBuilder::MapPropertyToBuilder

Verifica se um construtor deve ser associado a uma propriedade específica.

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

*dispid* \[ Em\]
</dt> <dd>

O DISPID da propriedade em questão.

</dd> <dt>

*pdwCtlBldType* \[ out\]
</dt> <dd>

O construtor a ser mapeado. Esse parâmetro pode ser uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                                          | Significado                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt> </dl>    | Invoque um construtor de sistema padrão (sem suporte no Visual Studio).<br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt> </dl> | Invocar um construtor personalizado.<br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt> </dl> | O construtor modifica o objeto . Esse é um comportamento comum.<br/>              |



 

</dd> <dt>

*pbstrGuidBldr* \[ out\]
</dt> <dd>

O GUID que identifica o construtor dessa propriedade.

</dd> <dt>

*builderAvailable* \[ out, retval\]
</dt> <dd>

Esse parâmetro será **TRUE** se essa propriedade atualmente dá suporte a um construtor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Vsp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IProvidePropertyBuilder**](iprovidepropertybuilder.md)
</dt> </dl>

 

 




