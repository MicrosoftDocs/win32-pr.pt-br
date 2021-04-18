---
description: Cria um objeto salvar que será usado para salvar dados em um arquivo. x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'Método ID3DXFile:: createsaveobject (D3DX9Xof. h)'
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
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771394"
---
# <a name="id3dxfilecreatesaveobject-method"></a>Método ID3DXFile:: createsaveobject

Cria um objeto salvar que será usado para salvar dados em um arquivo. x.

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

*pData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para o nome do arquivo a ser usado para salvar dados.

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[D3DXF \_ filesaveoptions](d3dxf.md)**

Valor que especifica o nome do arquivo no qual os dados serão salvos. Esse valor pode ser um dos sinalizadores de [Opções de salvamento de arquivo](d3dxf.md) .

</dd> <dt>

*dwFileFormat* \[ no\]
</dt> <dd>

Tipo: **[D3DXF \_ FileFormat](d3dxf.md)**

Indica o formato a ser usado ao salvar o arquivo. x. Esse valor pode ser um dos sinalizadores de [formatos de arquivo](d3dxf.md) . Para obter mais informações, consulte Comentários.

</dd> <dt>

*ppSaveObj* \[ fora\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Endereço de um ponteiro para uma interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , que representa o objeto salvar criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Comentários

Depois de usar esse método, use métodos da interface [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) para criar objetos de dados e para salvar modelos ou dados.

Para o formato de arquivo salvo *dwFileFormat*, um dos sinalizadores binário, binário herdado ou de texto nos [formatos de arquivo](d3dxf.md) deve ser especificado. O arquivo pode ser compactado usando o \_ sinalizador compactado FileFormat opcional D3DXF \_ .

Os valores de formato de arquivo podem ser combinados em uma lógica ou para criar texto compactado ou arquivos binários compactados. Se você indicar que o formato do arquivo deve ser texto e compactado, o arquivo será gravado primeiro como texto e, em seguida, compactado. No entanto, arquivos de texto compactados não são tão eficientes quanto arquivos de texto binários; na maioria dos casos, portanto, você desejará indicar binário e compactado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
