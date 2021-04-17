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
ms.openlocfilehash: 77fa2e5a0d387fcc0c90417b5f57d49178bc0626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754909"
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

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido, o valor de retorno será **S \_ OK**. Caso contrário, o valor de retorno será um código de erro.

## <a name="remarks"></a>Comentários

Quando a contagem de janelas do navegador atinge zero no modo Web integrado, essa função libera os carregadores de classe Java. Quando o usuário começa a procurar novamente os applets, a VM Java baixará os arquivos de classe mais recentes.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
