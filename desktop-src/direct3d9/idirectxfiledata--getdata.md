---
description: Recupera os dados para um dos membros do objeto ou os dados de todos os membros. Preterido.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'Método IDirectXFileData:: GetData (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811721"
---
# <a name="idirectxfiledatagetdata-method"></a>Método IDirectXFileData:: GetData

Recupera os dados para um dos membros do objeto ou os dados de todos os membros. Preterido.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*szMember* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ponteiro para o nome do membro para o qual recuperar dados. Especifique **NULL** para recuperar todos os dados dos membros necessários.

</dd> <dt>

*pcbSize* \[ fora\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para receber o tamanho do buffer ppvData, em bytes.

</dd> <dt>

*ppvData* \[ fora\]
</dt> <dd>

Tipo: **void \* \***

Endereço de um ponteiro para o buffer para receber os dados associados a szMember. Se szMember for **NULL**, ppvData será definido para apontar para um buffer que contém todos os dados dos membros necessários em um bloco contíguo de memória.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será DXFILE \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDATAREFERENCE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Comentários

Esse método recupera os dados para os membros necessários de um objeto de dados, mas não dados para Membros (filho) opcionais. Use [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) para recuperar objetos filho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 
