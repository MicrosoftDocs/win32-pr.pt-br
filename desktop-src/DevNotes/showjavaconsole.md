---
description: A função ShowJavaConsole é um recurso de depuração para desenvolvedores de Java. Os applets (ou outro código Java) em execução no Internet Explorer podem usá-lo para exibir mensagens de erro e outras informações.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: Função ShowJavaConsole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 0a8517d32057b6434d3822cc02977f6afd72c1b387b78e85e53810bd27f00550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075850"
---
# <a name="showjavaconsole-function"></a>Função ShowJavaConsole

A função **ShowJavaConsole** é um recurso de depuração para desenvolvedores de Java. Os applets (ou outro código Java) em execução no Internet Explorer podem usá-lo para exibir mensagens de erro e outras informações.

## <a name="syntax"></a>Sintaxe


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

<dl></dl>

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Chamar **ShowJavaConsole** faz com que a VM (máquina virtual) do Java exiba a janela do console do Java. A própria janela do console do Java pode exibir a saída de depuração do código Java em execução no processo de chamada. Normalmente, isso seria usado somente por um aplicativo que hospeda a VM Java. Há apenas uma única janela de console Java por processo; várias chamadas para a API resultam na mesma janela exibida. Em outras palavras, se a janela do console já estiver sendo exibida, nada acontecerá; se a janela não tiver sido exibida ou o usuário a tiver fechado, a janela será exibida.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
