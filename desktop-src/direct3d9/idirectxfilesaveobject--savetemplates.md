---
description: Salva modelos em um arquivo DirectX. Preterido.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: Método IDirectXFileSaveObject::SaveTemplates (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 87ec95932b26877354c22089a97b249bd542aa841552c3e3f9e4827a20f6d608
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292217"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>Método IDirectXFileSaveObject::SaveTemplates

Salva modelos em um arquivo DirectX. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cTemplates* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número total de modelos a salvar.

</dd> <dt>

*ppguidTemplates* \[ Em\]
</dt> <dd>

Tipo: **const [**GUID**](guid.md) \* \***

Endereço de um ponteiro para uma matriz dos GUIDs para salvar todos os modelos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

O fragmento de código a seguir fornece uma chamada de exemplo para **IDirectXFileSaveObject::SaveTemplates** e o conteúdo de exemplo para a matriz para a qual ppguidTemplates aponta.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Depois de usar esse método para salvar os modelos, use o [**método IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) para criar um objeto de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
