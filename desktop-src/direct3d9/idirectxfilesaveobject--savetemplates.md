---
description: Salva modelos em um arquivo do DirectX. Preterido.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'Método IDirectXFileSaveObject:: SaveTemplates (DXFile. h)'
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
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298583"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a>Método IDirectXFileSaveObject:: SaveTemplates

Salva modelos em um arquivo do DirectX. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cTemplates* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número total de modelos a serem salvos.

</dd> <dt>

*ppguidTemplates* \[ no\]
</dt> <dd>

Tipo: **[**GUID**](guid.md) \* \* const**

Endereço de um ponteiro para uma matriz de GUIDs para todos os modelos a serem salvos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

O fragmento de código a seguir fornece uma chamada de exemplo para **IDirectXFileSaveObject:: SaveTemplates** e conteúdo de exemplo para a matriz para a qual ppguidTemplates aponta.


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



Depois de usar esse método para salvar os modelos, use o método [**IDirectXFileSaveObject:: Createdataobject**](idirectxfilesaveobject--createdataobject.md) para criar um objeto de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileSaveObject](idirectxfilesaveobject.md)
</dt> <dt>

[**IDirectXFileSaveObject:: createdataobject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 
