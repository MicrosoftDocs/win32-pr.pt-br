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
ms.openlocfilehash: cbcb53aae008423ac56bb489d43f6fd78016a9b1f716be21390a6dfc1de00404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162060"
---
# <a name="extract-function"></a>Extrair Função

\[Essa função não tem mais suporte, portanto, seu comportamento não pode ser garantido.\]

A **função Extract** extrai arquivos de um gabinete.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ps* 
</dt> <dd>

Ponteiro para uma [**estrutura SESSION**](session.md) que contém informações sobre a sessão atual.

</dd> <dt>

*lpCabName* 
</dt> <dd>

Ponteiro para o nome do gabinete do qual os arquivos devem ser extraídos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela **retornará S \_ OK;** caso contrário, retornará um código de erro.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Erf**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**Sessão**](session.md)
</dt> </dl>

 

 
