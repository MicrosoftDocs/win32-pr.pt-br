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
ms.openlocfilehash: eb4012a04b4da9e353a5d771f9b9e61d4bfba8b45ed6a7d5c65a81c197ff9be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075740"
---
# <a name="verifycatalogfile-function"></a>Função VerifyCatalogFile

\[Não há suporte para essa função e não deve ser usada.\]

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

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará **ERROR \_ SUCCESS**; caso contrário, retornará o erro de [**WinVerifyTrust.**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)

Se o catálogo for um catálogo assinado por Authenticode, essa função retornará **ERROR \_ AUTHENTICODE \_ TRUSTED \_ PUBLISHER** se for bem-sucedido; caso contrário, retornará **ERROR \_ AUTHENTICODE \_ TRUST NOT \_ \_ ESTABLISHED**.

Se a função não puder determinar se o publicador é confiável, ela também poderá retornar **ERRO \_ NÃO IDENTIFICADO \_ ERRO.**

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
