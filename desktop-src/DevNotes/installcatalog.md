---
description: Instala um catálogo em um diretório.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: Função InstallCatalog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756513"
---
# <a name="installcatalog-function"></a>Função InstallCatalog

\[Essa função não tem suporte e não deve ser usada.\]

Instala um catálogo em um diretório.

## <a name="syntax"></a>Sintaxe


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CatalogFullPath* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que representa o caminho completo do catálogo antes da instalação.

</dd> <dt>

*NewBaseName* \[ em, opcional\]
</dt> <dd>

Um ponteiro para o novo nome de base.

</dd> <dt>

*NewCatalogFullPath* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que representa o caminho completo do catálogo após a instalação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não está implementada no momento, portanto, não retorna um valor real.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
