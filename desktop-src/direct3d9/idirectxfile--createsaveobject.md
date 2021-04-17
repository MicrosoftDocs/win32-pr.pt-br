---
description: Cria um objeto salvar. Preterido.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'Método IDirectXFile:: createsaveobject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105749418"
---
# <a name="idirectxfilecreatesaveobject-method"></a>Método IDirectXFile:: createsaveobject

Cria um objeto salvar. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do arquivo a ser usado para salvar dados.

</dd> <dt>

*dwFileFormat* \[ no\]
</dt> <dd>

Tipo: **[ **DXFILEFORMAT**](dxfile.md)**

Indica o formato a ser usado ao salvar o arquivo do DirectX. Esse valor pode ser um dos sinalizadores DXFILEFORMAT \_ XXX em [constantes DXFILE](dxfile.md). Para obter mais informações, consulte Comentários.

</dd> <dt>

*ppSaveObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

Endereço de um ponteiro para uma interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) , que representa o objeto salvar criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Depois de usar esse método, use métodos da interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) para criar objetos de dados e para salvar modelos ou dados.

O valor padrão para o formato de arquivo é DXFILEFORMAT \_ binário. Os valores de formato de arquivo podem ser combinados em uma lógica ou para criar texto compactado ou arquivos binários compactados. Se um arquivo for especificado como binário (0) e texto (1), ele será salvo como um arquivo de texto porque o valor será indistinguíveis do valor de formato de arquivo de texto (0 + 1 = 1). Se você indicar que o formato de arquivo deve ser texto e compactado, o arquivo será gravado primeiro como texto e, em seguida, compactado. No entanto, arquivos de texto compactados não são tão eficientes quanto arquivos de texto binários, portanto, na maioria dos casos, você desejará indicar binário e compactado. Definir um arquivo a ser compactado sem especificar um formato resultará em um arquivo binário e compactado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 
