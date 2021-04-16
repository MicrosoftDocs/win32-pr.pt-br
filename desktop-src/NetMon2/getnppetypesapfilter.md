---
description: A função GetNPPEtypeSapFilter recupera o filtro ETYPE/SAP de um determinado BLOB.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Função GetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758592"
---
# <a name="getnppetypesapfilter-function"></a>Função GetNPPEtypeSapFilter

A função **GetNPPEtypeSapFilter** recupera o filtro ETYPE/SAP de um determinado BLOB.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB.

</dd> <dt>

*pnSaps* \[ fora\]
</dt> <dd>

Ponteiro para o número retornado de protocolos na tabela SAP.

</dd> <dt>

*pnEtypes* \[ fora\]
</dt> <dd>

Ponteiro para o número retornado de ETYPEs na tabela ETYPE.

</dd> <dt>

*ppSapTable* \[ fora\]
</dt> <dd>

Ponteiro para a tabela SAP retornada.

</dd> <dt>

*ppEtypeTable* \[ fora\]
</dt> <dd>

Ponteiro para a tabela de ETYPE retornada.

</dd> <dt>

*pFilterFlags* \[ fora\]
</dt> <dd>

Ponteiro para os sinalizadores de filtro retornados.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

Identificador para um BLOB de erro, que especifica o local no BLOB original onde o erro (se houver) ocorreu.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="remarks"></a>Comentários

As informações de ETYPE/SAP são armazenadas na categoria de **configuração** da seção de **proprietário** NPP.

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

[SetNPPEtypeSapFilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




