---
description: A função DllGetVersion recupera o número de versão de Cabinet.dll usando a estrutura CABINETDLLVERSIONINFO.
ms.assetid: 93f6c29e-6a62-46c2-a42b-8270fe522494
title: Função DllGetVersion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: e04fd8bc520f037c89912af730c537159867219e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751586"
---
# <a name="dllgetversion-function"></a>Função DllGetVersion

\[Essa função não é mais suportada, portanto, seu comportamento não pode ser garantido.\]

A função **DllGetVersion** recupera o número de versão de Cabinet.dll usando a estrutura [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) .

## <a name="syntax"></a>Sintaxe


```C++
VOID WINAPI DllGetVersion(
   PCABINETDLLVERSIONINFO pcdvi
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcdvi* 
</dt> <dd>

Ponteiro para a estrutura [**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md) que contém as informações de versão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CABINETDLLVERSIONINFO**](cabinetdllversioninfo.md)
</dt> <dt>

[**GetDllVersion**](getdllversion.md)
</dt> </dl>

 

 
