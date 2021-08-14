---
description: Define o filtro do BLOB ETYPE/SAP.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Função SetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 30b2f6ffbefad955034f520162b6fdc44d80198d926f35443ce21fefd80ef5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363822"
---
# <a name="setnppetypesapfilter-function"></a>Função SetNPPEtypeSapFilter

A função **SetNPPEtypeSapFilter** define o filtro do blob ETYPE/SAP.

## <a name="syntax"></a>Sintaxe


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Um identificador para o BLOB.

</dd> <dt>

*nSaps* \[ no\]
</dt> <dd>

O número de SAPs.

</dd> <dt>

*nEtypes* \[ no\]
</dt> <dd>

O número de ETYPEs na tabela ETYPE que está sendo definida.

</dd> <dt>

*lpSapTable* \[ no\]
</dt> <dd>

Um ponteiro para a tabela SAP que está definida.

</dd> <dt>

*lpEtypeTable* \[ no\]
</dt> <dd>

Um ponteiro para a tabela ETYPE definida.

</dd> <dt>

*FilterFlags* \[ no\]
</dt> <dd>

Os sinalizadores de filtro definidos.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

O identificador para um BLOB de erro que especifica onde ocorreu o erro (se houver) no BLOB original.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[GetNPPEtypeSapFilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




