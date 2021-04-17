---
description: Instala um arquivo de catálogo.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: função pSetupInstallCatalog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748495"
---
# <a name="psetupinstallcatalog-function"></a>função pSetupInstallCatalog

\[Esta função não é mais suportada pela Microsoft. Os desenvolvedores devem usar o **CryptCATAdminAddCatalog**.\]

Instala um arquivo de catálogo.

## <a name="syntax"></a>Sintaxe


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CatalogFullPath* \[ no\]
</dt> <dd>

O caminho totalmente qualificado do catálogo a ser instalado no sistema.

</dd> <dt>

*NewBaseName* \[ no\]
</dt> <dd>

O novo nome de base a ser usado quando o arquivo de catálogo é copiado para o repositório de catálogo.

</dd> <dt>

*NewCatalogFullPath* \[ out, opcional\]
</dt> <dd>

Opcionalmente, recebe o caminho totalmente qualificado do arquivo de catálogo no repositório de catálogo. Esse buffer deve ter no mínimo bytes de **\_ caminho máximo** (versão ANSI) ou caracteres (versão Unicode).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função tiver êxito, ela **não retornará nenhum \_ erro**; caso contrário, ela retornará um código de erro Win32 que indica a causa da falha.

## <a name="remarks"></a>Comentários

O arquivo é copiado pelo sistema em um diretório especial e, opcionalmente, é renomeado.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CryptCATAdminAddCatalog**](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
