---
description: Libera carregadores de classe Java que podem ter sido consumidos ao navegar pelos applets.
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: Função NotifyBrowserShutdown
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 60f361d8f9963081c4af2a840a01eb29f9946eb064cad2335f95b3622932add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826812"
---
# <a name="notifybrowsershutdown-function"></a>Função NotifyBrowserShutdown

Libera carregadores de classe Java que podem ter sido consumidos ao navegar pelos applets.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpvReserved* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem sucedido, o valor de retorno será **S \_ OK**. Caso contrário, o valor de retorno será um código de erro.

## <a name="remarks"></a>Comentários

Quando a contagem de janelas do navegador atinge zero no modo Web integrado, essa função libera os carregadores de classe Java. Quando o usuário começa a procurar novamente os applets, a VM Java baixará os arquivos de classe mais recentes.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
