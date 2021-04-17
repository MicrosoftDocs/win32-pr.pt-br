---
description: Verifica um único arquivo de catálogo.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: Função VerifyCatalogFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748925"
---
# <a name="verifycatalogfile-function"></a>Função VerifyCatalogFile

\[Essa função não tem suporte e não deve ser usada.\]

Verifica um único arquivo de catálogo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CatalogFullPath* 
</dt> <dd>

O caminho totalmente qualificado do arquivo de catálogo a ser verificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, ela retornará **\_ êxito de erro**; caso contrário, retornará o erro de [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).

Se o catálogo for um catálogo assinado por Authenticode, essa função retornará um **erro de \_ \_ \_ Publicador de Authenticode confiável** se tiver sucesso; caso contrário, ele retornará um **erro de confiança de \_ Authenticode \_ \_ não \_ estabelecida**.

Se a função não puder determinar se o Publicador é confiável, ele também poderá retornar **um \_ \_ erro de erro não identificado**.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
