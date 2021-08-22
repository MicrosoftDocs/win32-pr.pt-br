---
description: Cria um objeto save. Preterido.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: Método IDirectXFile::CreateSaveObject (DXFile.h)
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
ms.openlocfilehash: c3646f54b1f232c6eec3e1b3d06441a8e6a7c090f784e3c4c016f7f1bcfc3b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491846"
---
# <a name="idirectxfilecreatesaveobject-method"></a>Método IDirectXFile::CreateSaveObject

Cria um objeto save. Preterido.

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

*szFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do arquivo a ser usado para salvar dados.

</dd> <dt>

*dwFileFormat* \[ Em\]
</dt> <dd>

Tipo: **[ **DXFILEFORMAT**](dxfile.md)**

Indica o formato a ser usado ao salvar o arquivo DirectX. Esse valor pode ser um dos sinalizadores DXFILEFORMAT \_ xxx em [constantes DXFILE](dxfile.md). Para obter mais informações, consulte Comentários.

</dd> <dt>

*ppSaveObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

Endereço de um ponteiro para uma interface [**IDirectXFileSaveObject,**](idirectxfilesaveobject.md) representando o objeto save criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Depois de usar esse método, use métodos da interface [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) para criar objetos de dados e salvar modelos ou dados.

O valor padrão para o formato de arquivo é DXFILEFORMAT \_ BINARY. Os valores de formato de arquivo podem ser combinados em um OR lógico para criar texto compactado ou arquivos binários compactados. Se um arquivo for especificado como binário (0) e texto (1), ele será salvo como um arquivo de texto porque o valor será indistinguível do valor de formato de arquivo de texto (0 + 1 = 1). Se você indicar que o formato de arquivo deve ser texto e compactado, o arquivo será gravado primeiro como texto e compactado. No entanto, os arquivos de texto compactados não são tão eficientes quanto os arquivos de texto binário, portanto, na maioria dos casos, você deseja indicar binário e compactado. Definir um arquivo a ser compactado sem especificar um formato resultará em um arquivo binário compactado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 
