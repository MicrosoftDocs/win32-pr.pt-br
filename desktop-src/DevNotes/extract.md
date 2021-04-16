---
description: A função Extract extrai arquivos de um gabinete.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Extrair Função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747882"
---
# <a name="extract-function"></a>Extrair Função

\[Essa função não é mais suportada, portanto, seu comportamento não pode ser garantido.\]

A função **Extract** extrai arquivos de um gabinete.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*profissionais* 
</dt> <dd>

Ponteiro para uma estrutura de [**sessão**](session.md) que contém informações sobre a sessão atual.

</dd> <dt>

*lpCabName* 
</dt> <dd>

Ponteiro para o nome do gabinete do qual os arquivos devem ser extraídos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido, ela retornará **S \_ OK**; caso contrário, retornará um código de erro.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**SESSÃO**](session.md)
</dt> </dl>

 

 
