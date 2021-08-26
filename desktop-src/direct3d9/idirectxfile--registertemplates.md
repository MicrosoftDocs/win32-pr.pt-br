---
description: Registra modelos personalizados. Preterido.
ms.assetid: f9b24800-83a5-45bf-b19f-b247c88a2c2c
title: Método IDirectXFile::RegisterTemplates (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 685e97ec28241348ff4a969c444b6da5638aeba01af8be35cc5490a0d2be0a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846956"
---
# <a name="idirectxfileregistertemplates-method"></a>Método IDirectXFile::RegisterTemplates

Registra modelos personalizados. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RegisterTemplates(
  [in] LPVOID pvData,
  [in] DWORD  cbSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pvData* \[ Em\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro para um buffer que consiste em um arquivo DirectX em formato de texto ou binário que contém modelos.

</dd> <dt>

*cbSize* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Tamanho do buffer apontado por pvData, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: \_ DXFILEERR BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR \_ BADFILEVERSION, DXFILEERR \_ BADVALUE, DXFILEERR \_ PARSEERROR.

## <a name="remarks"></a>Comentários

O fragmento de código a seguir fornece uma chamada de exemplo para **RegisterTemplates** e conteúdo de exemplo para o buffer para o qual o pvData aponta.


```
    TIDirectXFile * pDXFile;
    char *szTemplates = "xof 0303txt 0032\
        template SimpleData { \
            <2b934580-9e9a-11cf-ab39-0020af71e433> \
            DWORD item1;DWORD item2;DWORD item3;} \
        template ArrayData { \
            <2b934581-9e9a-11cf-ab39-0020af71e433> \
            DWORD cItems; array DWORD aItem[2][cItems]; [...] } \
        template RestrictedData { \
            <2b934582-9e9a-11cf-ab39-0020af71e433> \
            DWORD item; [SimpleData]}";
    hr = pDXFile->RegisterTemplates(szTemplates, strlen(szTemplates));
    
    
```



Todos os modelos devem especificar um nome e um UUID (Identificador Universal Exclusivo).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> </dl>

 

 
