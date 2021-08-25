---
description: Cria um objeto save que será usado para salvar dados em um arquivo .x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: Método ID3DXFile::CreateSaveObject (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: aaf9f884a651182429de20fe261a250c8c6567eacd99d635213682e4d755b79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951606"
---
# <a name="id3dxfilecreatesaveobject-method"></a>Método ID3DXFile::CreateSaveObject

Cria um objeto save que será usado para salvar dados em um arquivo .x.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o nome do arquivo a ser usado para salvar dados.

</dd> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ARQUIVOS D3DXFAVEOPTIONS \_](d3dxf.md)**

Valor que especifica o nome do arquivo no qual os dados devem ser salvos. Esse valor pode ser um dos [sinalizadores Opções de Salvar](d3dxf.md) Arquivo.

</dd> <dt>

*dwFileFormat* \[ Em\]
</dt> <dd>

Tipo: **[ \_ FILEFORMAT D3DXF](d3dxf.md)**

Indica o formato a ser usado ao salvar o arquivo .x. Esse valor pode ser um dos [sinalizadores Formatos](d3dxf.md) de Arquivo. Para obter mais informações, consulte Comentários.

</dd> <dt>

*ppSaveObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFileSaveObject,**](id3dxfilesaveobject.md) que representa o objeto save criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Comentários

Depois de usar esse método, use métodos da interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) para criar objetos de dados e salvar modelos ou dados.

Para o formato de arquivo salvo *dwFileFormat*, um dos sinalizadores binário, binário herdado ou de texto em [Formatos](d3dxf.md) de Arquivo deve ser especificado. O arquivo pode ser compactado usando o sinalizador \_ OPCIONAL FILEFORMAT COMPRESSED D3DXF. \_

Os valores de formato de arquivo podem ser combinados em um OR lógico para criar texto compactado ou arquivos binários compactados. Se você indicar que o formato de arquivo deve ser text e compactado, o arquivo será gravado primeiro como texto e compactado. No entanto, os arquivos de texto compactados não são tão eficientes quanto os arquivos de texto binários; na maioria dos casos, portanto, você deseja indicar binário e compactado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
